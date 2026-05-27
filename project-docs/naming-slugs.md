# Naming and slugs

## Reel slugs

Each reel gets a *slug* that is used consistently across folders and filenames.

### Pattern

- Base:  
  `[maker]-[model]`
  Example: `penn-720`
- If there is a model number or size:
  `[maker]-[model]-[model-number]`
  Example: `pfleuger-pelican-1020`
- If there is a variant:
  `[maker]-[model]-[model-number](if applicable)-[variant]`
  Example: `zebco-33-hudson-bay-red`

### Rules

- All lowercase
- Use hyphens between all words and codes
- In general do not use production years-*may* be used to distinguish variants

### Where slugs are used-examples

Project folder
  - Overview: `docs/[maker]/[slug]-overview.md`
  - Service guide: `docs/[maker]/[slug]-guide.md`

Workspace
  - Substack drafts: `.../substack/[slug]/[slug]-new-arrival.md`
  - etc.
  - Video scripts: `.../youtube/[slug]-overview script.docx`
  - etc.

Media folders
  - Pictures: `Pictures/vintage reel service guides/[maker]/[model]/[slug]-[desc].jpg`  ← all images
  - Video: `Video/vintage reel service guides/[maker]/[model]/[overview, service guide]/[slug]-[desc].[mlt, mkv, rpp, wav, mp4]`

.mlt = Shotcut project file
.mkv = Shotcut file
.mp4 = final output file for YouTube
.wav = voiceover
.rpp = Reaper file