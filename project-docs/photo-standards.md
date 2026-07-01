# Photo standards

## Basic photos - initial session for new reels

Taken before the reel is serviced and also after. Used in overview, also possibly in service guide, on substack posts, etc.
  - Multiple views of whole reel - front, handle-side, badge / drag-side, top, bottom, back, left (angled left), right (angled right)  - these will be candidates for hero images
  - Badge or nameplate
  - Exterior/special features (varies with reel, i.e., drag lever)

Details: Hero images should show what makes each reel *visually distinctive*, like the badge, finish, or proportions - while this can be more or less generalized for each reel type, e.g., for spinning reels the handle side is usually more interesting, and the bail should be rotated to show it off - it will be somewhat different for each reel, and this will contribute to the unique take on each reel.

## Disassembly and reassembly photos

Taken while working on reel in tray.
  - At least one image per user action/step. For some steps two or three images to show progression of more intricate moves.
  - Hands are always in frame.
  - Tools are always shown in use.
  - Maintain a clean workspace to reduce visual distractions. Only show tools actually in use on a specific reel.
  - Keep parts neatly organized in tray so all are clearly visible.

## Cleaning and lubrication photos

Cleaning and lubricating are covered in a generic document, but if there are any reel-specific cleaning/lubricating procedures for a specific reel, photograph those.

## File naming standards / slugs

Having consistent filenames for images will facilitate all current work and any future refactoring. The basic goal is to have descriptive but brief, self-explanatory filenames which will work in the repo, and which help provide a map through each procedure.

  - Basic example form is `[slug]-[description].jpg`
  
  - Always use hyphens (for compatability with repo).
  
  - Descriptions in filenames - when it's an action, leave off suffixes, e.g., "align" not "aligning."

  - Describe reel position by front, back, handle side, and badge / drag side (not left, -1, etc.)

  - If schematic is available, use part names from schematic, e.g., "eccentric"

Use numbers sparingly and consistently:

  - If a filename includes a number, it must indicate a *sequence*.

    Example: penn-720-remove-main-gear-1.jpg, penn-720-remove-main-gear-2.jpg = step progresses through a multi‑stage action or different angles of the same step.

  - For two or more slightly different *versions* of a shot, prefix with v1, v2, etc.

    Example: penn-720-hero-front-v1.jpg, penn-720-hero-front-v2.jpg = alternative candidates you’re evaluating; only one may end up in the guide.

  - Keep a simple photo-standards.md with sections like verbs, states, views, suffixes (-ref, -v1, -v2). Each time you invent a new term while renaming (lift, separate, inspect, hero-front, etc.), add it there and keep using the same spelling.
  
    - **Verbs**: align, clean, remove, grease, replace, lubricate, reassemble, test.

    - **States**: engaged / disengaged, pre-service, removed.

    - **Views**: front, handle-side, badge / drag-side, top, bottom, back, on-rod, left (angled left), right (angled right).

    - **Suffixes**: -ref (reference-only sets), -1, -2 (different views, generally higher numbers mean "more" - closer, larger angle, etc.) -v1/-v2 (versions, alt takes of same shot), numeric sequences for true progressions, `[processing]` like auto-contrast, etc., `[###]`px if resized.

    - **Usage**: hero- (used only when curating / copying / renaming files to project folder), -ref (used for files only used for internal reference, like unusable disassembly images).

    - **Features**: badge / logo, drag, cork-arbor, foot (often has writing on it), anti-rev (anti-reverse lever).

### Naming workflow

1. Import images from card to workspace `/[maker]/[model]/`
2. Open folder in XnView, r-click, batch rename to `[maker]-[model]`
Filenames by default will have numeric suffix.

## Camera settings

For Olympus PL1 camera body.

  - Use 3 x 3 grid.
  
  - Shoot white card for white balance: Press start / OK, select capture WB icon, press info, point camera at white card, press shutter, select yes. If the camera can't set WB based on what's in front of it - low light, etc. - there will be error message WB NG RETRY.

Using focus modes - for lenses with manual focus ring (e.g., the macro lens):

See p. 44 in PL-1 manual for full details

To set basic mode:

Menu > gears > AM / MF > AF mode > still picture / movie > S-AF+MF (auto-focus + allows fine manual adjustment) / MF (full manual control)

To turn off MF assist (if on, this zooms to 10x when using manual focus to assist with fine adjustments - but it can be distracting):

/ AM / MF > MF assist on / off

## Lenses

### m.zuiko digital ED 14-42mm 1:3.5-5.6 lens

  - Manual setting
  - ISO 200
  - f11
  - 1/10 sec
  - 2 sec timer
  - focal length ~ 27 mm (varies with shots)

Short version:

14-42mm 1:3.5-5.6 default setup: M, ISO 200, f11, 1/10 s, 2 s timer, focal length ~ 27 mm (varies with zoom), camera distance X (see diagram), custom WB from white card.

These settings seem to work well for full-body hero shots of spinning reels. [need to doc distance - 13" i think]

For closer macro shots f8, .4 s seems to work [need to doc distance, 1 / should be .10 meter].

### m.zuiko digital ED 30 mm 1:3.5 macro lens

30mm macro default setup: M, ISO 200, f11, 1/10 s, 2 s timer, fixed focal length = 30 mm, camera distance X (see diagram), custom WB from white card.

magnification is from 1/4 x - 1.25 x
subject distance = .20 mm - .095 mm
exposure comp. = + 1/3 - +2 (not needed for auto mode)

Practical working distances: about 20 cm for full‑reel hero shots (≈0.25×), and roughly 6 cm for tight badge/part details (≈1–1.25×).

Usable aperture range tested: f7.1 to f13 all producing solid images, with plans to compare f8 vs f11 more carefully at the hero distance.

Focusing workflow that finally felt comfortable: MF Assist off, using MF or S‑AF+MF as needed, with the focus ring behaving predictably on the PL1.

### Grids

To turn on and select type.

MENU > [two gears icon] > DISP/PC > /INFO SETTING > LV-Info > Displayed Grid [4 types or off]

During shooting use INFO to toggle selected grid on/off.

For details see in the workspace `photo-video-grids-framing.md`, also see PL-1 manual p. 44.

## Framing/positioning

Heros:  Reel positioned as if mounted on rod, for example, for spinning reels the foot should be at top. Reel front facing left, center of front lower 3rd, handle side facing camera, handle at diagonal.

## XnView settings

for image size, output dirs, levels, etc.

## Video cam settings

Software is [Guvcview](https://guvcview.sourceforge.net/) loaded on an ubuntu laptop.

On startup select cam. Use preset 3.
  - Resolution: 1920x1080
  - Frame rate: 30 fps
  - Video codec: H.264
  - Container format: .mkv files

## Video export settings

Software is [Shotcut](https://www.shotcut.org) loaded on a Windows desktop. Export preset is YT1080p30 stack. This outputs an MP4 file with H.264 video and AAC audio, optimized for YouTube. Custom settings, based on h.264 main profile:

Video tab
  - Resolution: 1920x1080
  - Frame rate: 30 fps
  - Codec: libx264 (H.264)
  - Rate control: Averabe bitrate (ABR) or CBR
  - Bitrate: 8 mb/s (good quality, manageable file size)

Audio tab
  - Codec: AAC
  - Sample rate: 48000 Hz
  - Channels: Stereo
  - Bitrate: 128 kb/s

File sizes, approx., at 8Mb/s
  - 1.5 min clip ~ 90 Mb
  - 4 min clip ~ 256 Mb

For longer videos (~10 min) it might be good to try 6Mb/s to reduce file size.

## Geometry

Describe position of hero box, tray, light and camera rigs, overall workspace, lights. Draw on graph paper and photograph, insert image here.

## Lighting

Describe lights, intensity, color temp, diffusion fabric.

NEO

## Saving images, naming standards, slugs, and dirs for image files

All images are saved as jpg files. For image workflow, see [project workflow](project-workflow.md).

For details on naming and slugs see [naming slugs](naming-slugs.md).

For details on dirs see [directory layout](directory-layout.md).