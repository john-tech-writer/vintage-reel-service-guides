# Project Workflow

1. Select reel based on roadmap for volumes, acquire. See [Volume Planning](volume-planning.md). This file includes a record of what's been done and what needs to be done for each reel.

2. Acquire all available documentation for the reel. Schematics, box inserts, user manuals, articles. ORCA archive, US patent office, ask Perplexity.ai. If documents and/or box is included with reel, take photos and save in project folder. Add an entry to [References](../../references.md).

2. Take initial pictures of reel, standard set. For more details see [Photo Standards](photo-standards.md)

3. Write substack post for the "welcome to the bench" series.
  - Use template/example E://documents/vintage-reel-service-guides/docs/project-docs/welcome-bench-magic-fishing-reel-example.md, save as E://documents/1-vintage reel service guide project/substack/welcome-bench-maker-model-number.md
  - Post to substack, tag as "new arrival" (this is the tag corresponding to "welcome to the bench."
  - Wiring to repo: The post template includes a connections section which includes a link to the repo and notes that when the overview and guide are published there, a notification will be posted on substack.
  Wiring to YT: Create substack video for posting to YouTube.

4. Post substack vid to YT.

5. Write overview using Notepad ++ based on template in , save as .md file as E://documents/vintage-reel-service-guides/docs/maker/maker-model-number-overview.md

Notes: Currently (may 2026) there doesn't seem to be a need to create subdirectories for each model, i.e., E://documents/vintage-reel-service-guides/docs/maker/model/maker-model-number-overview.md and it just seems to add unnecessary complexity, also would require some work on existing published docs--Penn 720 and Pflueger Nobby--but in the future it might become desirable as the library grows.

6. Write script for overview based on skeleton and example in E://documents/vintage-reel-service-guides/docs/project-docs, save as E://documents/1-vintage reel service guide project/video scripts/script maker model number-overview.docx

Notes: The skeletons and examples should be in the project folder as .md files so they can eventually be pushed to a github repo to (1) document the project workflow for my personal use, and (2) to use as a basis for the "how to build a stack" future project. The reel-specific scripts however should be saved as .docx files for easy printing and reading while recording the vids. There is no simple way to print reader-friendly .md files. Also they should be saved (as noted) in the project working docs folder since the reel-specific files don't belong in the repo.

7. Capture video for overview using logitech cam and guvcview on laptop.
  - Save as .mpv
  - Copy to stick
  - Copy to office machine, to 

8. Write service guide using Notepad ++ based on template in, save as .md file in 

9. Capture video for service guide using logitech cam and guvcview on laptop.

10. Upload to YouTube.
  - Write description based on template


13. Commit and push; confirm GitHub Pages update.


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