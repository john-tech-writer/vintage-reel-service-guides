# Parking lot: switch MkDocs project to a virtual environment

**Why:** On 7/27/2026, `py -m mkdocs` failed with `No module named mkdocs` because the `py` launcher's default Python had changed to 3.14 since the original February setup, and MkDocs (plus its plugins) were installed under an older Python version. A venv pins the exact Python + packages to this project folder so future Python installs on the machine can never break it again.

**Trigger to come back to this:** after a break, whenever ready to stop babysitting Python versions for this project.

---

## Step 1 — Create the virtual environment

From the project root:

```
E:\documents\vintage-reel-service-guides> py -m venv venv
```

## Step 2 — Activate it (do this every new terminal session)

```
E:\documents\vintage-reel-service-guides> venv\Scripts\activate
```

Prompt should now show `(venv)` at the start of the line. Run `deactivate` to exit the venv when done.

## Step 3 — Install MkDocs and this project's plugins inside the venv

Based on the current `mkdocs.yml` (theme: readthedocs, plugins: search + mermaid2, markdown_extensions: attr_list, md_in_html, pymdownx.superfences):

```
(venv) E:\documents\vintage-reel-service-guides> pip install mkdocs mkdocs-mermaid2-plugin pymdown-extensions
```

(`readthedocs` theme, `search` plugin, `attr_list`, and `md_in_html` are all bundled with MkDocs core — no separate install needed for those.)

## Step 4 — Confirm it works

```
(venv) E:\documents\vintage-reel-service-guides> mkdocs --version
(venv) E:\documents\vintage-reel-service-guides> mkdocs serve
```

No `py -m` prefix needed once the venv is active — `mkdocs` becomes its own command.

## Step 5 — Add venv to .gitignore (do NOT commit the venv folder to Git)

Check if `.gitignore` exists yet:
```
E:\documents\vintage-reel-service-guides> dir /a .gitignore
```

If it doesn't exist, create it — command line is easier than Explorer/Notepad for dotfiles:
```
E:\documents\vintage-reel-service-guides> type nul > .gitignore
```
Then open it in Notepad++ (File > Open, set filter to "All types (*.*)" or it may not show up) and add:
```
venv/
```
Or create + write directly from Notepad:
```
E:\documents\vintage-reel-service-guides> notepad .gitignore
```
(Click "Yes" when it asks to create a new file — this avoids Notepad silently appending .txt.)

## Step 6 — Freeze package versions for your own records

```
(venv) E:\documents\vintage-reel-service-guides> pip freeze > requirements.txt
```

## Step 7 — Check the GitHub Actions workflow matches

The live GitHub Pages build runs independently of your local venv, using whatever install step is defined in the repo's workflow file. Since `mermaid2` and `pymdown-extensions` were added locally, the workflow needs them too or the live site build could fail (or mermaid diagrams could render broken) even though local `mkdocs serve` works fine.

Find the file:
```
E:\documents\vintage-reel-service-guides> dir .github\workflows
```

Open whichever `.yml` shows up (e.g. `pages.yml`, `deploy.yml`):
```
E:\documents\vintage-reel-service-guides> notepad .github\workflows\<filename>.yml
```

Look for a step running something like `pip install mkdocs` or `pip install -r requirements.txt`. If it's missing `mkdocs-mermaid2-plugin` and `pymdown-extensions`, that step needs updating (ideally to `pip install -r requirements.txt` once Step 6's file exists, so local and CI always stay in sync).

---

## Notes for future reference

- `py -0p` lists every Python version installed on the machine and flags the default with an asterisk — useful for a quick sanity check before this ever happens again.
- Currently on Python 3.14 (the newest release as of July 2026) — no urgent need to update further; MkDocs is a local static-site tool, not processing untrusted input, so there's no security urgency driving Python version updates here.
