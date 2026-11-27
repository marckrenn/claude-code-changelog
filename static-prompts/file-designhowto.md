One AppifactRepl call per board, all calls in one message (parallel tool calls), in reading order. Call it as {artifact: <the new Artifact's url>, code}. The calls run one at a time, in the order you send them, each as soon as its block is complete, so the page shows each board the moment its call returns, while you are still writing the next.
The canvas is kept as files under `project/`, none of it in the store. The FIRST call writes only the canvas's index, `project/canvas.json`, giving EVERY planned board its place and size, and no board:
```js
const files = await claude.use("files"), fs = require("fs"), path = require("path");
const index = "project/canvas.json", made = (await files.list()).some(f => f.path === index);   // the page may have made the index already: keep its keys
const canvas = { v:3, launch:{view:"canvas"}, pages:[], notes:{}, designSystems:[], attachments:{}, createdOnFiles:{ v:1, at:new Date().toISOString() }, ...(made ? JSON.parse(await files.read(index)) : {}) };
canvas.title = title;
canvas.boards = { "Main.dc.html":{ x:0, y:0, w:880, h:560 }, "Pricing.dc.html":{ x:960, y:0, w:880, h:560 } };
canvas.order = ["Main.dc.html","Pricing.dc.html"];
canvas.designSystemTokens = require("<the tokens.json path above>");   // only with a design system
fs.mkdirSync(path.join(files.dir(), "project"), { recursive: true });
fs.writeFileSync(path.join(files.dir(), index), JSON.stringify(canvas));
await files.publish({ file_path: index });
```
Then one call per board, each a complete small program of its own, with the html typed inline:
```js
const files = await claude.use("files"), fs = require("fs"), path = require("path");
const board = "project/Main.dc.html", file = path.join(files.dir(), board);
fs.mkdirSync(path.dirname(file), { recursive: true });
fs.writeFileSync(file, `<div>...</div>`);
await files.publish({ file_path: board });
```
The index names every planned board, so each later call writes only its own new file (a named board with no file yet keeps its place and shows once its file lands). Each program starts fresh: no call uses a variable of an earlier one, and each has its own `files.dir()`, removed when it ends, so a call publishes what it writes. These calls stand in for Artifact publishes and for ArtifactData, write_db and read_db calls on this canvas. With a design system, the colours, type and spacing are the ones in the files you printed.
Make the design with markup unless the user asked for the real components by name; design-system-components.md above says how.
A revision works the same way: one message, one call per changed board, each reading the file it changes before it changes it:
```js
const files = await claude.use("files"), fs = require("fs"), path = require("path");
const board = "project/Pricing.dc.html", file = path.join(files.dir(), board), html = await files.read(board);
fs.mkdirSync(path.dirname(file), { recursive: true });
fs.writeFileSync(file, html.replace("£12", "£14"));
await files.publish({ file_path: board });
```
If a call reports an error, fix the line it names and send THAT call again, not the others. If the error names a file that changed or was not read, add a `files.read` of that file to the call.
