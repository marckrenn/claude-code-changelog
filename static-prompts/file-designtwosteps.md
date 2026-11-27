[This canvas in two steps] Everything this canvas needs is already on disk, in the files listed with this note. Two steps make the design.

Step 1, one message: the Bash call or calls the notes give, if any, copied as they are. In that same message, read this artifact's url with the Artifact tool (the read call given below, the url alone, no path): it returns the type's instructions (SKILL.md) and records that you have seen this version. Unless the user says they have written in it, the canvas is new and empty: the read is for the instructions and the version, not for content. You do not need the ArtifactData tool, Read, Skill or ToolSearch for any of this, nor a second read step: everything else is already printed. Where the printed instructions tell you to read one of the type's reference pages, that reading is this step: those pages are on disk, and the ones you need are the ones you have just printed.

Step 2, one message: for this NEW canvas, where the section below says "Create: one call", send instead one AppifactRepl call per artboard, each called as `{artifact: <this Artifact's url>, code}`, ALL in this one message (parallel tool calls), in reading order, after ONE first call that writes only the canvas's frame, and no board. The canvas is kept as files under `project/`, nothing in the store: the index is `project/canvas.json` and each artboard is `project/<its file name>`. The FIRST call, the frame alone:
```js
const files = await claude.use("files");
const fs = require("fs"), path = require("path");
// the index: read it when it is listed, else start it with its createdOnFiles key; give EVERY planned artboard its boards entry and its place in order, keep every other key, publish that one file
const listed = (await files.list()).some(f => f.path === "project/canvas.json");
const canvas = listed ? JSON.parse(await files.read("project/canvas.json")) : { v:3, launch:{ view:"canvas" }, pages:[], boards:{}, order:[], notes:{}, designSystems:[], attachments:{}, createdOnFiles:{ v:1, at:new Date().toISOString() } };
canvas.title = title;
canvas.boards = { "Main.dc.html": { x:0, y:0, w:880, h:560 }, "Pricing.dc.html": { x:960, y:0, w:880, h:560 } };
canvas.order = ["Main.dc.html","Pricing.dc.html"];
fs.mkdirSync(path.join(files.dir(), "project"), { recursive: true });
fs.writeFileSync(path.join(files.dir(), "project/canvas.json"), JSON.stringify(canvas, null, 2) + "\n");
await files.publish({ file_path: "project/canvas.json" });
```
Then one call per artboard, each a complete small program of its own that creates its board's file, with the `html` typed inline once (its place and size are in the frame):
```js
const html = `<div>...</div>`;
const files = await claude.use("files");
const fs = require("fs"), path = require("path"), file = path.join(files.dir(), "project/Main.dc.html");
fs.mkdirSync(path.dirname(file), { recursive: true });
fs.writeFileSync(file, html); // ONE new file, published alone
await files.publish({ file_path: "project/Main.dc.html" });
```
The next board's program is the same with its own path: `project/Pricing.dc.html`.
The frame names every planned artboard, so a later call writes only its own new file: no read first, no index rewrite, no placeholder (a named artboard with no file yet keeps its place and shows once its file lands). The frame comes first on purpose: an artboard file the index does not name yet is shown at a place the page picks, and an open tab may record that place. Each program has its own `files.dir()`, removed when it ends, so a call publishes what it writes. Each program starts fresh: no call uses a variable of an earlier one. The calls run one at a time, in the order you send them, each as soon as its block is complete, so each artboard is published the moment its call returns, while you are still writing the next: send them in the order a reader would want to see them. These calls stand in for Artifact publishes and for ArtifactData, write_db and read_db calls on this canvas.
Make the design with markup in these two steps unless the user asked for the real components by name; the type's design-system-components page, which is on disk, says how.
A revision works the same way: one message, one call per changed artboard, each reading what it changes before it changes it (with `files.read`).

If a call reports an error, fix the line it names and send THAT call again, not the others; write_db is not needed for that, nor another read of the artifact unless the error asks for one: the url read in step 1 still counts as having seen this version. If the error names a file that changed or was not read, add a `files.read` of that file to the call.
