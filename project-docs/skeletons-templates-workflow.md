# Skeletons and templates

Templates typically just provide a form - headings and a few prompts. Skeletons provide form plus some example content. Templates and skeletons provide a starting point for every content file. They enforce standards for form, headings, style, and content.

Best‑practice pattern for document templates / skeletons development:

  - A concrete worked example (existing published guide, reel stack, etc.) with most of the content removed, just a few concrete examples.

  -  Light inline guidance / prompts layered on top (italic hints: *here’s why this name works*, *this is where the template comes from*, etc.).

The form is never blank - it always provides both real content plus minimal commentary. Over time, after a few of these combo docs stabilize, a more generic template can always be abstracted from it if that is needed for speed or sharing (a sanitized version, for example, for a generic how-to project on the repo).

## Repo skeletons

Live in the project folder `project-docs/repo skeletons/`

Usage: Creating the source files for overviews and service guides on the repo. Open in Notepad ++, Save As to the project folder `docs/[maker]-[slug]-[overview / service-guide].md.` These files get pushed to the repo.

##YouTube skeletons / templates

Live in the workspace `youtube/skeletons-templates/` and on YouTube.

Usage:

  - Creating video scripts. Open in Notepad ++, Save As to the workspace `youtube/[slug]-[overview / service-guide / #]-script.md.` These files get printed for benchtop use when recording the videos. These may be throwaways after the videos are completed.

  - Creating YouTube descriptions. Local md files are mostly for reference and backup, to compare with descriptions on the YouTube channel and enforce standards. May be Saved As if needed for temporary use. Most drafting can be done on YouTube.

Workflow:

In YouTube > Studio > Content > Videos > select a video of the same type > pencil icon / details > copy title / details > paste into new video description

There may be some back and forth between the local description example and the online draft for convenience in drafting but there is no need to save most of these descriptions locally since they are fairly generic. One or two examples of each type are enough.

### Video templates

Live in the Video media folder `templates/`

Usage: These are Shotcut mlt project files, creating new projects in Shotcut for overview and service guide videos. They provide the basic structure for video projects, text standards, and rough timings.

Open, Save As.

## Substack skeletons / templates

Live in the workspace `substack/skeletons-templates/` and on Substack.

Usage: Creating substack posts, one per series, slug is series display / title name.

Local md files are mostly for reference and backup, to compare with posts on Substack and enforce standards. May be Saved As if needed for temporary use. Most drafting can be done on Substack. However since these can be longer documents a local copy may be useful.

Copy and paste the text from the final post in Substack into an empty md file in Notepad ++, Save As to the workspace `substack/[slug]/[slug]-[service-guide-final / etc.].md.` These files are used for local drafting and backup / archiving content.

Workflow:

In Substack > Posts > Drafts > open the skeleton for the type of post being drafted > select all / copy > Create > Article > paste > start drafting in Substack / paste into a new md doc > save in workspace `substack/[slug]/[slug]-[title].md

There will be a good bit of back and forth between the Substack draft and local draft. After the local file is finalized and the post scheduled / published, append -final to filename.

