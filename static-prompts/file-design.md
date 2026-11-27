[How to build and iterate on Design canvases efficiently] This canvas's content lives in files under `project/`, nothing in the store: the index is `project/canvas.json`, and each board is `project/<key>`, where <key> is its key in the index's `boards`. Read each file you will change by its `path` and publish the changed ones back with `file_path` and `files`; include `project/canvas.json` only when you add, remove, reorder, move or resize a board or change anything else it holds, changing just those keys. If the AppifactRepl tool is among your tools, use it for this canvas instead of separate Artifact calls: do all of that inside one program, as the examples below show: `files.list()`, `files.read` or `files.readMany` for what you change, the new text written into `files.dir()`, ONE `files.publish`. One call runs a short JavaScript program against this canvas's files: a whole design lands in one step. Call it as `{artifact: <this Artifact's url>, code}`. Never write_db / read_db this canvas. Images and font files upload from inside the program, one call per file: put the file in `files.dir()`, then `(await claude.use("assets")).upload(path)` answers `{url, id}`, and each returned `url` goes in verbatim where the board names it.

Create: one call.
```js
const files = await claude.use("files");
const fs = require("fs"), path = require("path"), dir = files.dir();
fs.mkdirSync(path.join(dir, "project"), { recursive: true });
// 1 · the index: read it when it is listed, else start it with its createdOnFiles key; every artboard's boards entry and its place in order, every other key kept
const listed = (await files.list()).some(f => f.path === "project/canvas.json");
const canvas = listed ? JSON.parse(await files.read("project/canvas.json")) : { v:3, launch:{ view:"canvas" }, pages:[], boards:{}, order:[], notes:{}, designSystems:[], attachments:{}, createdOnFiles:{ v:1, at:new Date().toISOString() } };
canvas.title = title;
canvas.boards = { "Main.dc.html": { x:0, y:0, w:880, h:560 }, "Pricing.dc.html": { x:960, y:0, w:880, h:560 } };
canvas.order = ["Main.dc.html","Pricing.dc.html"];
fs.writeFileSync(path.join(dir, "project/canvas.json"), JSON.stringify(canvas, null, 2) + "\n");
// 2 · one file per artboard
fs.writeFileSync(path.join(dir, "project/Main.dc.html"), mainHtml);
fs.writeFileSync(path.join(dir, "project/Pricing.dc.html"), pricingHtml);
// 3 · ONE publish: file_path = one file, files = the others
await files.publish({ file_path: "project/canvas.json", files: { "project/Main.dc.html": "project/Main.dc.html", "project/Pricing.dc.html": "project/Pricing.dc.html" } });
```

Revise: read it back in the SAME program that writes, change only what was asked, one call. Each call starts fresh. When you must see existing files first, do all the looking in ONE program that prints only what you need (the listing, `project/canvas.json`, the parts of files you will match): read every file you need in one program, with one `files.readMany([paths])` (their texts come back in that order); then ONE program that reads, writes and publishes. The writing program reads, with `files.read` or `files.readMany`, every EXISTING file it replaces or removes, `project/canvas.json` included, before it publishes: a listing alone does not count, and a publish over a file it did not read may be refused; new files need no read.
```js
const files = await claude.use("files");
const fs = require("fs"), path = require("path");
// 1 · read every existing file you change, the index too; write the new text into files.dir() at the same relative paths
const [index, pricing] = await files.readMany(["project/canvas.json", "project/Pricing.dc.html"]);
const canvas = JSON.parse(index);
const dir = files.dir();
fs.mkdirSync(path.join(dir, "project"), { recursive: true });
fs.writeFileSync(path.join(dir, "project/Pricing.dc.html"), pricing.replace("£12", "£14"));
// a new artboard: its file, plus the index with its boards entry and its path in order, every other key kept
fs.writeFileSync(path.join(dir, "project/Faq.dc.html"), faqHtml);
canvas.boards["Faq.dc.html"] = { x: 1920, y: 0, w: 880, h: 560 };
canvas.order.push("Faq.dc.html");
fs.writeFileSync(path.join(dir, "project/canvas.json"), JSON.stringify(canvas, null, 2) + "\n");
// 2 · ONE publish: file_path = one changed file, files = the others
await files.publish({ file_path: "project/canvas.json", files: { "project/Pricing.dc.html": "project/Pricing.dc.html", "project/Faq.dc.html": "project/Faq.dc.html" } });
```
Send `project/canvas.json` only when the layout changes, and keep every key of it you are not changing, its `createdOnFiles` or `convertedFrom` key included. Publish only files under `project/`: never `index.html`, `SKILL.md` or anything under `artifact-type/`. Files you leave out stay as they are; `"project/Old.dc.html": null` in `files` removes one you have read, with `project/canvas.json` sent too, its `boards` entry and its path in `order` taken out. If the publish is refused because someone saved in the meantime, or names files that changed, run this program again from its first line, once: its reads pick up their version. If it names files that were not read, add a `files.read` of each to the program first. If it says you have not viewed the latest version, read the canvas's url with the Artifact tool once, then run the program again. Any other refusal: tell the user what it said and stop. Print only what you need from a file, never whole bodies you do not need: the output is capped.

Every shape and limit above still applies. With that tool, do not use write_db or read_db for this canvas; without it, follow the steps above.
