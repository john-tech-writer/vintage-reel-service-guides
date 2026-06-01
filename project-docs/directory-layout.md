# Directory layout

## 1. Project folder

Local clone of `vintage-reel-service-guides` repository on Github

- `vintage-reel-service-guides/`
  - `.git/`
  - `.github/`
  - `docs/`
    - `img/`
      - `[maker]/`
        - `[model]/`
          - `[slug]-[image-desc].jpg`  ← final images used in repo
    - `[maker]/`
      - `[slug]-overview.md`  ← final docs used in repo
      - `[slug]-service-guide.md`
      - `penn-spinfisher-series.md`  ← example-other *reel-specific* docs used in repo
    - `about.md`  ← generic (*non-reel-specific*) docs used in repo
    - `index.md`  ← repo landing page for project documentation
    - `references.md`
    - `baitcasting-reels.md`
    - etc.
  - `project-docs/`  ← docs about repo standards, org., and content development
    - `repo templates/`
      - `overview-template-example.md`
      - `guide-template-example.md`
    - `project-workflow.md`
    - `naming-slugs.md`
    - `directory-layout.md`
    - etc.  ← other files that will be published on the repo, linked in either nav or other files
  - `site/`  ← built site files

## 2. Workspace

Active working documents that do **not** go in the repo

- `vintage-reel-service-guides-workspace/`
  - `general referece docs/`
    - `general-reference.md`  ← writing references
    - `reel collection.docx`
  - `how-to class outlines/`
  - `maker and reel docs/`
    - `spinning-general/`
    - `[maker]`
    - `[maker] [desc]`
    -  or
      - `[slug]-[desc].[ext]`
    - `penn/`  ← for example
    - `penn production archive.pdf`
    - or
      - `penn-700-series-manual.pdf`
      - etc.
  - `project development-background/`
    - `audio-troubleshooting-win.docx`
    - `design-badge notes.docx`
    - `docs-mermaid-flowcharts-mkdocs.docx`
    - `photo-lighting-fixing glare-polarizing.docx`
    - `README.md`← describes purpose for this folder and file naming conventions, read this first
    - `video-adding-audio-shotcut.md`
    - `z-review of first vid-burke drama ideas--other bits--old version.md`
    - etc.  ← 30+ docs, mostly .docx
  - `reel-balanced tackle disc/`
    - `garcia 3000-4000 disc.pdf`  ← for example
    - etc.
  - `substack/`
    - `[slug]/`
      - `[slug]-new-arrival.md`
      - `[slug]-production-notes.md`
      - `[slug]-field-stories.md`
      - `[slug]-new-publication`
    - `youtube/`
    - `[slug]/`
      - `[slug]-overview script.docx`
      - `[slug]-disassembly script.docx`
      - `[slug]-reassembly script.docx`
      - `[slug]-youtube desc.docx`  ← descriptions for all YT vids
    - `templates`
      - `overview-script template-example.docx`
      - `service-script template-example.docx`  ← for both service vids
      - `youtube desc template-example.docx`

## 3. Pictures

All raw and edited photos

- `Pictures/vintage reel service guides/`
  - `[maker]/`
    - `[model]/`
      - `[slug]-[desc].jpg`
  - `assets-banners-logos/`
  - `fish images/`
  - `jigs for reel repair/`
  - `workspace-bench/`

## 4. Video

All captured footage and edits

- `Video/vintage reel service guides/`
  - `general/`
  - `[maker]/`
    - `[model]/`
      - `[slug]-overview.mp4/`  ← final videos used on YouTube
      - `[slug]-disassembly.mp4/`
      - `[slug]-reassembly.mp4/`