# MkDocs commands - command prompts

## Getting started

Type command prompt in search and open a window.

E: to switch drives

cd \documents\vintage-reel-service-guides to change dirs, this is where mkdocs is installed on my machine currently and probably forever, just makes sense

## Restoring command prompt after serve command

If after a serve, don't have a command prompt anymore, do this.

MkDocs serve is a long‑running foreground process, so while it’s serving you shouldn’t get a new prompt. You don’t need to close the window, though—just stop the server.

With the command prompt window active press:

Ctrl + C

This shuts down the server and you're back with a command line prompt.

In that same terminal window to stop py -m mkdocs serve --livereload ...; it will exit back to a normal E:\...> prompt.

So your workflow becomes:

1.	Open terminal, start server:
E:
cd "\documents\Vintage Reel Service Guides"
py -m mkdocs serve --livereload --watch docs

2.	Leave that window running while you edit; it rebuilds on each save.

3.	When you’re done for now, press Ctrl + C once (or twice) in that window to stop MkDocs and get your prompt back.

## Reinstalling MkDocs after Python upgrade

From the root:

E:\documents\vintage-reel-service-guides> py -m pip install mkdocs mkdocs-mermaid2-plugin pymdown-extensions

Then verify and serve:

E:\documents\vintage-reel-service-guides> py -m mkdocs --version
E:\documents\vintage-reel-service-guides> py -m mkdocs serve

Copy / paste the url into browser to review locally.

## Live preview

Usage: to be able to serve an md file locally and view changes on the fly in the browser. useful for table formatting.

Run: py -m mkdocs serve

Copy / paste the url into browser to review locally.

Run: py -m mkdocs serve --live-reload

Working in Notepad++, make edits, save. They will display in real time in the browser.