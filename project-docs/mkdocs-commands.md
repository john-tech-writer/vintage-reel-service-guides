Restoring command prompt after serve command

If after a serve, don't have a command prompt anymore, do this.

MkDocs serve is a long‑running foreground process, so while it’s serving you shouldn’t get a new prompt. You don’t need to close the window, though—just stop the server.

On Windows, use:
Ctrl + C

In that same terminal window to stop py -m mkdocs serve --livereload ...; it will exit back to a normal E:\...> prompt.[127][128][129]

So your workflow becomes:

1.	Open terminal, start server:
E:
cd "\documents\Vintage Reel Service Guides"
py -m mkdocs serve --livereload --watch docs

2.	Leave that window running while you edit; it rebuilds on each save.

3.	When you’re done for now, press Ctrl + C once (or twice) in that window to stop MkDocs and get your prompt back.