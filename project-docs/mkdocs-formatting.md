# MkDocs Formatting

## Links

### Links to files
  - In the same dir: `[Alt text](filename.md)`

For example, from `vintage-reel-service-guides/project-docs/mkdocs-formatting` to `vintage-reel-service-guides/project-docs/photo-standards` is `[Photo Standards](photo-standards.md)`

  - In a dir one level up: `[Alt text](../dir/filename.md)`
For example, from `vintage-reel-service-guides/project-docs/mkdocs-formatting` to `vintage-reel-service-guides/docs/references` is `[References](../docs/references.md)`

Each ../ goes up one level in the dir structure, so two levels up would be ../../

  - From `/docs/` to a subfolder, add the subfolder. For example, from `/docs/schematics.md` to `/docs/magic/magic-fishing-reel-patent.pdf` is `[Original patent](magic/magic-fishing-reel-patent.pdf)` Note: no leading slash.

  - If the target is in a different dir/subdir off the root, add the path: `(../img/dir/dir/filename.md)`
  
  - Within the same file / page: `[display text](#heading-text)

Notes: if within same file type link is used as a list, e.g., a TOC / nav, each entry must be separated by a blank line and bulleted in order to display correctly as a list.

For example, `[Disassembly I](#disassembly-I)` will link to `##Disassembly I`

From a file in `/docs/` (a general file like references.md) up to one of the reel files like `/penn/penn-720-overview.md`: `[link text]([dir]/[filename]`, e.g., `[Penn 70 overview](penn/penn-overview.md)`

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

Format as shown in this example will number correctly. You can use 1s for all steps and they will renumber correctly when pushed to the repo. This is useful when initially authoring steps where there may be a lot of additions, deletions, etc. so you don't have to keep renumbering them.

This format also supports figure captions and the <figcaption> tag supports inserting a link and / or emphasis in the caption.

Main points: Number starts at right margin, blank lines must be truly blank, no spaces, etc., all lines of the <figure> must be indented 4 spaces.

1. Remove the crank nut and crank / handle.

    <figure markdown>
    ![Pflueger Nobby No. 1963 - removing crank / handle](../../img/pflueger/nobby/pflueger-nobby-1963-remove-crank-1.jpg)
    <figcaption>Pflueger Nobby model No. 1963 - removing crank / handles</figcaption>
    </figure>

    Use a 3/8" socket wrench. A screwdriver can also be used but the socket has the virtue of being less likely to damage the nut, especially if it is hard to turn.

2. Remove the cap screws (3).

## Tables

Usage: formatted tables. note that this does not depend on Mermaid, which is only for flowcharts and similar elements.

Species | Comments
-|-
![Black bass - from Pflueger 1935 catalog](../../img/fish/black-bass-w-text.jpg) | Wide range of sizes

Model | Production years | Colors | Features
--|--|--|
*No. 1963* | 1935 - 1957 | blue / satin aluminum<br>cream marbled handles | level wind<br>grease disc
*No. 1963C* | 1954 - 1971 | satin chromium<br>white handles | -
*No. 1960 Deluxe* | 1957 - 1967 | maroon<br>tan handles | hollow gears<br>nylon bearings<br>cork arbor
*No. 1965 Free Spool* | 1964 - 1971 | red<br>gray marbled handles | push-button free spool<br>star drag

Troubleshooting: if table does not format correctly when built:

  - count the pipe-split segments in the separator row and compare against the header's cell count
  - check Encoding > UTF-8
  - check blank lines before / after table

# Creating a two-column layout

Usage: for example, creating pages with images on one side and text on the other.

What actually works well: md_in_html + a custom CSS class

Good news — your mkdocs.yml already has everything needed for the clean approach (attr_list and md_in_html are both already enabled, and you've got extra_css: stylesheets/extra.css wired up). This pattern works with any theme, not just Material — it's core Python-Markdown behavior:

In the page markdown:

<div class="two-col" markdown="1">
<div class="two-col-img" markdown="1">
![Nobby cover engraving](../images/nobby-cover.jpg)
</div>
<div class="two-col-text" markdown="1">
Text about the Nobby's history goes here, and it can include **markdown** formatting, links, etc.
</div>
</div>

Then add this once to stylesheets/extra.css:

.two-col {
  display: flex;
  gap: 1.5rem;
  align-items: flex-start;
  margin: 1.5rem 0;
}
.two-col-img { flex: 0 0 40%; }
.two-col-img img { width: 100%; height: auto; display: block; }
.two-col-text { flex: 1; }

@media (max-width: 768px) {
  .two-col { flex-direction: column; }
}

