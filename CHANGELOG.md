# Changelog

What changed in the two latest versions of Kadr. More on the official website: https://kadr.uk/

## [1.1.0-beta.27] - 2026-10-24

### New

- **Kadr's own music** — Library → Audio → Music → «Kadr music»: choose a mood (calm, documentary, tense, upbeat, epic,
  emotional), tempo and length (the project's length by default) and Kadr composes an original instrumental bed — no
  samples, so it cannot get a copyright claim. Listen first, then add it at the playhead; long videos get several
  beds joined smoothly. When you have no YouTube Audio Library folder, own music or Epidemic Sound connected, the AI
  uses Kadr's music and tells you once how to connect a better source.

### Fixed

- Since beta.25 the AI could add no music and no sound effects at all when no music source was set up (tester report).
  Free sound effects (CC0 and CC BY, credited in the export) are allowed again; music-like tracks, NC/ND licences and
  Kevin MacLeod stay excluded.
- When Kadr refuses something to the AI several times in a row, it now tells the AI to stop retrying, and bug reports
  show why it was refused.

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
