# Project workflow

1. Select reel based on [volume planning](volume-planning.md), acquire.

    Add an entry for the reel in reel collection.docx in [workspace](directory-layout.md) `/maker and reel docs/general reference docs/`. This file is a record of when each reel was acquired, cost, origin, and notes on what's been done/needs to be done for each reel.

1. Acquire all available documentation for the reel, save to [workspace](directory-layout.md) in `/maker and reel docs/[maker]/[slug]-[desc].[ext]`. Add an entry to [References](../docs/references.md).

    - If documents and/or box is included with reel, take photos and save in [project folder](directory-layout.md) in `/docs/[maker]`. These these images are treated as documents and included in the project so users can view them using the link provided in the References page.
    - If documents are obtained from other sources, the files are not included in the project. The source link will be provided in the References page but users may need to pay to view the documents (e.g., ORCA online archives).

1. Take initial pictures of reel using [Photo Standards](photo-standards.md). Save to [Pictures](directory-layout.md) in `/maker and reel docs/[maker]/` as `[slug]-[desc].jpg`.

1. Open pictures folder using [XnView](https://www.xnview.com/en/xnview/) and edit as necessary:

    - Crop and rotate.
    - Size (standards?), auto contrast and levels using Tools > Batch convert > Actions tab
Most of these actions are already saved in XnView but can be checked/unchecked, edited, etc.
    - Save to [project folder](directory-layout.md) in `/docs/img/[maker]/[model]/[slug]-[desc].jpg` using Tools > Batch convert > Output tab

1. Write substack post for "welcome to the bench" series.
    - Use template in [project folder](directory-layout.md) `/project-docs/templates`, save to workspace `/substack/[slug]/welcome-bench-[slug].md`.
    - For help with developing content, see [Substack Ideas](substack-ideas.md) and post examples--[Welcome to the Bench](substack-welcome-bench-example.md).
    - Post to substack, tag as "new arrival" (corresponds to "welcome to the bench" post series).
    - Wire to repo: Post template includes a connections section with link to the repo, notes that when the entire stack is published a notification will be posted on substack.
    - Wire to YT: Connections section includes link to YT. Create substack video for posting to YouTube.

1. Post substack vid to YT.
    - Wire to substack:
    - Wire to repo:

1. Write overview using template in [workspace](directory-layout.md) in `/repo templates/` and save in [project folder](directory-layout.md) as `/docs/[slug]-overview.md.` This will get pushed to the repo.

1. Write service guide using template in [project folder](directory-layout.md) in `/repo templates/` and save in [project folder](directory-layout.md) as `/docs/[slug]-service-guide.md.` This will get pushed to the repo.

1. Write script for overview based on skeleton and example in E://documents/vintage-reel-service-guides/docs/project-docs, save as E://documents/1-vintage reel service guide project/video scripts/script maker model number-overview.docx

    Notes: The skeletons and examples should be in the project folder as .md files so they can eventually be pushed to a github repo to (1) document the project workflow for my personal use, and (2) to use as a basis for the "how to build a stack" future project. The reel-specific scripts however should be saved as .docx files for easy printing and reading while recording the vids. There is no simple way to print reader-friendly .md files. Also they should be saved (as noted) in the project working docs folder since the reel-specific files don't belong in the repo.

1. Capture video for overview using logitech cam and guvcview on laptop.
    - Save as .mpv
    - Copy to stick
    - Copy to office machine, to 

1. Write service guide using Notepad ++ based on template in, save as .md file in 

1. Capture video for service guide using logitech cam and guvcview on laptop.

1. Upload to YouTube.
    - Write description based on template

1. Commit and push; confirm GitHub Pages update.

# Content standards
- Titles: pattern, capitalization rules.
- Filenames: `penn-720-service.md`, `penn-720-step-01.jpg`, etc.
- Section structure: Overview, Tools, Disassembly, Cleaning, Lubrication, Reassembly, Variants.

# Release checklist
- Spellcheck and style check.
- Confirm all images load.
- Post/update links on YouTube and ORCA.

# Reference-commands for command line version of github
This is not needed if using the github gui
- Start local preview: `py -m mkdocs serve`
- Stop preview: `Ctrl + C`
- Build site: `py -m mkdocs build`
- Check git status: `git status`
- Commit changes: `git commit -am "Message"`
- Push to GitHub: `git push`