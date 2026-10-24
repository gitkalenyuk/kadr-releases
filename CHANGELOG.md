# Changelog

What changed in the two latest versions of Kadr. More on the official website: https://kadr.uk/

## [1.1.0-beta.26] - 2026-10-24

### New

- **Photos and videos in your proportion** — a new «Photos & videos» chip in the AI chat brief and in channel
  profiles: a slider «Photos N % · Videos N %» (or Auto). The AI keeps the share of photos and video on screen within
  ±10 % of it, the rough cut aims for it, and «Check project» shows an error when the video is further off.
- **Repeat limits** — how many times one video fragment and one photo may appear in a video (1 = never repeat, up to
  10, or no limit), separately for video and photos, in the brief and the profile. The old «allow repeats» switch of a
  profile is converted by itself. A freeze frame next to its clip or a photo cut into several pieces in a row counts as
  one use.
- **When there is only one photo** of a person who is named many times, the AI asks you what to do (in the modes with
  questions). In Full auto it uses that photo at every mention with a different framing each time, never twice in a
  row, and says so in the chat with the times; «Check project» shows it as a warning, not an error.

## [1.1.0-beta.25] - 2026-10-24

### New

- **Music without copyright claims** — the AI now uses only safe music: Kadr's own sounds and music beds, recordings
  that are really in the public domain or CC0, tracks from your YouTube Audio Library folder and your own music. Tracks
  that often get Content ID claims (for example Kevin MacLeod / Incompetech, Jamendo, ccMixter, CC BY music) are no
  longer picked by the AI, and «Check project» warns about risky music already on the timeline. You can still add any
  track by hand — Kadr then shows a warning.
- **YouTube Audio Library** — Settings → Music: choose a folder with tracks you downloaded in YouTube Studio → Audio
  library and press Scan. Tracks that need a credit are marked, and the credit line goes into the export credits and
  the YouTube description by itself. The switch «Music only from YouTube Audio Library» (also in the chat brief) makes
  the AI use only these tracks.

### Improved

- **Footage sources checked one by one** — every video, photo and music source was tested with real downloads.
  Openverse photos and ccMixter download again. Sources that cannot work right now are switched off with the reason
  shown in Settings → Footage (Bilibili until its downloader is fixed, Europeana video, DigitalNZ audio), and the AI
  no longer wastes time on them. Empty and preview-only items are skipped.
- **Competitor channel analysis** runs in the background and the AI follows it, so a long analysis is no longer cut
  off after 5 minutes. A channel analysed in the last 24 hours is reused at once.
- **Long AI commands** (footage imports, exports) are no longer dropped by Claude Code while they work.
- **Website** and **What's new** in Kadr now open the official site kadr.uk and the release notes.

### Fixed

- The round Stop / Send buttons of the AI chat were squeezed into ovals in a narrow chat.
- Licences "no derivatives" (ND) and "non-commercial" (NC) were treated as free to use.
