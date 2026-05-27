# MkDocs Formatting

## Links

### Links to files
  - In the same dir: `[Alt text](filename.md)`
  
For example, from `vintage-reel-service-guides/project-docs/mkdocs-formatting` to `vintage-reel-service-guides/project-docs/photo-standards` is `[Photo Standards](photo-standards.md)`

  - In a dir one level up: `[Alt text](../dir/filename.md)`
For example, from `vintage-reel-service-guides/project-docs/mkdocs-formatting` to `vintage-reel-service-guides/docs/references` is `[References](../docs/references.md)`

Each ../ goes up one level in the dir structure, so two levels up would be ../../

  - From `/docs/` to a subfolder, add the subfolder. For example, from `/docs/schematics.md` to `/docs/magic/magic-fishing-reel-patent.pdf` is `[Original patent](magic/magic-fishing-reel-patent.pdf)` Note: no leading slash.

  - If the target is in a different dir/subdir off the root, add the path: (../img/dir/dir/filename.md)

### Adding links to site navigation

In root add filename to `mkdocs.yml`:

  - `Reels - Overviews and Service:`  ← renders in blue all caps, no link
      - `Penn:`  ← renders with + sign, linked as dropdown
          - `Penn 720 Overview (Spinning): penn/penn-720-overview.md`  ← render as links to doc
          - `Penn 720 Service (Spinning): penn/penn-720-service-guide.md`

This example uses readthedocs mkdocs template; other templates would render the nav somewhat differently. For each nested level add 2 more spaces to the beginning of the line.

### Links to images

`![Alt text](path.jpg)`

For example, ![Penn 720--Front Left](../../img/penn/720/penn-720-front-left.jpg)

## iframes and YouTube

### Lazy loading for iframes

Allows YouTube embeds to load only as they are displayed on a scrolled page.

<iframe
  loading="lazy"
  src="https://www.youtube.com/embed/2c1ZWjAN6yU"
  title="Penn 720 Overview"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen>
</iframe>

### Thumbnail embed

A YouTube thumbnail.

<a href="https://www.youtube.com/watch?v=2c1ZWjAN6yU" target="_blank" rel="noopener">
  <img
    src="https://img.youtube.com/vi/2c1ZWjAN6yU/hqdefault.jpg"
    alt="Penn 720 Overview video"
    style="max-width: 100%; height: auto; cursor: pointer;">
</a>

### Fake player icon and embed

This gives the look of YouTube embed without the overhead.

<a href="https://www.youtube.com/watch?v=2c1ZWjAN6yU" target="_blank" rel="noopener"
   style="position: relative; display: inline-block;">
  <img
    src="https://img.youtube.com/vi/2c1ZWjAN6yU/hqdefault.jpg"
    alt="Penn 720 Overview video"
    style="display: block; max-width: 100%; height: auto;">
  <span style="
    position:absolute;
    top:50%; left:50%;
    transform:translate(-50%, -50%);
    width:64px; height:64px;
    border-radius:50%;
    background:rgba(0,0,0,0.6);
  ">
  </span>
</a>

## Numbered steps

The following format allows entering numbers for procedures in mkdocs for editing purposes which will also be stable when pushed to the repo. Note that as long as this formatting is used you can use 1s for all steps and they will renumber correctly when pushed to the repo.

**Steps**

Start at the left margin, e.g.:

1. Remove the drag cap...
2. Remove the spool...

**Content under a step**

For example, images and extra paragraphs.

Indent 4 spaces:

␣␣␣␣![image](...)

␣␣␣␣This is a good time to inspect...

For bulleted lists under steps, to keep autonumbering working correctly (if using 1s for all steps) you will need to always indent 4 spaces rather than starting the first level of bullets with 2 spaces.

**Blank lines inside a step**

Between paragraphs or images.

Leave them *truly* blank (no spaces), e.g.:

␣␣␣␣![image](...)
<empty line>
␣␣␣␣Next sentence...

**Between steps**

One normal blank line (no spaces), then the next step number.

