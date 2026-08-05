# Project workflow

This file provides the basic roadmap for navigating, creating, and managing all project content. Other key files:

- [README](README.md): Orientation to the internal project documentation.

- [Parking lot](parking-lot.md): List of project upgrades and ideas for future iterations.

- [Directory layout](directory-layout.md): Diagram of all project directories and notes on their contents.

## Workflow philosophy

**Let the real work teach what the theory should look like**. As project content is developed, the workflow can also be abstracted and made concrete. Iterations on lived and living, dynamic examples result in constant improvement.

Workflow documentation informs ongoing content development and the content development in turn informs the evolution of the workflow. This includes processes, naming standards, software tools, and all the rest of the machinery that moves the project forward and makes content stylistically coherent and repeatable.

This file is the **one place** to always return to push the project a little further: cleaning dirs, tightening steps, wiring pieces together.

Every pass makes the project flow better: clearer naming, better links, more honest reflection of how project work is actually accomplished, not some abstract ideal.

Leaning on it solves decision fatigue: if the stack feels overwhelming - slugs / naming, badge / design, Substack / narrative, YouTube / video, reels / content sourcing - `project-workflow.md` can be opened, reviewed, worked on, and will move the project one notch higher. **That counts**.

## Naming and slugs

All reels and other project content sources are assigned a slug for easy and consistent identification across all directories and usages.

See [Naming and slugs](naming-slugs.md).

## Skeletons and templates

All content is based on skeletons / templates which enforce evolving content standards and help jog memory and ideas.

See [Skeletons and templates workflow](skeletons-templates-workflow.md).

## Workflow - repo

1. Select reel based on [volume planning](volume-planning.md), acquire.

    Add an entry for the reel in workspace `reference docs and books/reel collection.docx`. This file is a record of when each reel was acquired, cost, origin, and notes on what's been done / needs to be done for each reel.

2. Acquire all available documentation for the reel, save in workspace `maker and reel docs/[maker]/[slug]-[desc].[ext]` and add entries to [References](../docs/references.md).

    Typical docs include schematics, parts lists, box inserts, user manuals, patents, and articles from the ORCA archives.

    If documents and / or box is included with reel, take photos and save in project folder `/docs/[maker]/[slug].[pdf / jpg / etc.]`. Also if docs are not copyrighted and are available outside pay walls (e.g., ORCA archives), then they can be included in the project. These images are treated as documents, linked from the References page, and included in the project so users can view them using the link provided in the References page.

    If documents are obtained from other sources, the files are not included in the project. The source link will be provided in the References page but users may need to pay to view the documents (e.g., ORCA online archives).

3. Take initial photos of reel using the standards in [Image workflow](image-workflow.md). Save to the Pictures media folder `/maker and reel docs/[maker]/[slug]-[desc].jpg`

    These images will be used initially / primarily for the repo overview. Secondarily some will be used later in the workflow for the repo service guide, videos, and substack posts - anywhere an image of the reel intact is useful.

    For info on how to use grids on the Olympus PL1 camera and in Shotcut, as well as principles of framing and grid use, see in the workspace `photo-video-grids-framing.md`

    After taking the initial pictures, sync updated project folders to Dropbox as described in [Backup workflow](backup-workflow.md)

4. Open Pictures folder using [XnView](https://www.xnview.com/en/xnview/) and batch rename / batch convert. See [Image workflow](image-workflow.md)

    Save to [project folder](directory-layout.md) in `docs/img/[maker]/[model]/[slug]-[desc].jpg` using Tools > Batch convert > Output tab

5. Write substack post for "Welcome to the bench" series.

See [Substack standards and series](substack-standards-series.md).

6. Write overview using skeleton in project folder `repo skeletons/` and save in project folder as `docs/[maker]/[slug]-overview.md.` This will get pushed to the repo.

7. Take a second round of images. Save to the Pictures media folder `/maker and reel docs/[maker]/sg/[slug]-[desc].jpg`

    These images will be used initially / primarily for the repo service guide. Some of the service guide images will also be taken from the overview images (reel intact). Secondarily some will be used later in the workflow for videos and substack posts - anywhere an image of the reel intact is useful.

    After taking the second round of photos, sync updated project folders to Dropbox as described in [Backup workflow](backup-workflow.md)

8. Write service guide using skeleton in project folder `repo skeletons/` and save in project folder as `docs/[maker]/[slug]-service-guide.md.` This will get pushed to the repo.

## Workflow - videos

1. Write script for overview video based on skeleton. See [Skeletons and templates workflow](skeleton-templates-workflow.md).

2. Capture video for overview using logitech cam and guvcview on laptop. See [Image workflow](image-workflow.md).

    Use a card or stick to transfer the raw video mkv file from the laptop / benchtop to the workstation.

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