# Video / audio workflow

Output: overview and service videos for YouTube.

Software

  - Notepad ++
  - Guvcview - on laptop - profile: vintage-reels.gpfl
  - Shotcut - service guide template.mlt, to view export settings View > Export > Advanced, YT 1080p30 stack v2
  - Reaper - FX: VO - small speaker / phone tilt, Render > Presets > All settings > VO master WAV 44k 24bit - 15 LUFS / -1 dBTP
  - Mbox control - preset: 2 - recording VOs

Hardware

  - Logitec HD Pro C920 webcam
  - Mbox studio
  - Audio-technica MB 1K mic
  - Rode headphones (model?)

1. Write script for overview video. Based on overview .md file for the repo and on the overview skeleton, print to use on benchtop.

overview-skeleton.md > `[slug]-overview.md`
overview-script-skeleton.md  > `[slug]-overview-script.md`

2. (On laptop / benchtop) Record overview video with scratch audio, save .mkv file to micro card for transfer to workstation.

`[slug]-overview.mkv`

3. Create project in Shotcut, based on template (.mlt file) import video (.mkv file).

overview template.mlt > `[slug]-overview.mlt`

4. Edit project in Shotcut, adding stills and text from overview on repo, also from schematics and articles saved in the workspace, trimming, etc.

5. Create project in Reaper using fx preset, record VO, save, export as .wav using presets.

`[slug] overview audio.rpp`
`[slug] overview.wav`

6. Import audio to project in Shotcut, minor edits.

7. Export project as .mp4 file using YouTube preset, review locally, make sure Windows audio is playing correctly (no extra compression, etc. - check audio control panel).

`[slug]-overview.mp4`

8. Upload .mp4 to YouTube, write video details with title and desc. based on skeleton, add to appropriate playlists (refer to playlists doc if needed).

youtube-video-details-skeleton.md > author in YouTube

9. Add title and video link to youtube-video-links.md

9. Go through the same sequence for service videos 1, 2, and any additional shorts. For steps 7 / 8, service videos will also have markers as chapters exported from Shotcut as a .txt file and pasted into the YouTube description.

`[slug]-service-[#]-of[#]-chapter-markers.txt`