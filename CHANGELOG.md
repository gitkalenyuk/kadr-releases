# Changelog

What changed in the two latest versions of Kadr. More on the official website: https://kadr.uk/

## [1.1.0-beta.28] - 2026-10-26

### New

- **Genre in the AI chat brief** — pick the direction of the video (true crime, history, science, nature, travel,
  tech, business, kids, Shorts and more), the language and the length, and Kadr fills in everything else by itself:
  editing style, templates, kinds of graphics, transitions, photos vs video, repeats, music and captions. Every chip
  stays visible and editable; «Back to automatic» restores the genre's choice.
- **Pieces from one video** — a new limit in the brief and in channel profiles: at most N pieces from one source
  video (3 by default when fragments must not repeat). It counts found and downloaded footage only, never your own
  recordings.
- **Your own long recordings** — heavy files (4K, high bitrate, long) get a light preview copy in the background,
  the timeline stays smooth with hundreds of clips, and the AI finds scenes through scene lists and contact sheets
  instead of playing whole files. Editing a project with 600 clips is several times faster.
- **Your profile vs this chat** — before a run Kadr compares your channel profile with the brief and warns about
  conflicts (for example «YouTube first is the slowest source: expect ~N min of downloads»), with a «Fix the profile»
  button.
- **Weak model warning** — the model picker and the chat say when a model is too weak for editing (Haiku-class and
  small models) and offer to switch to Sonnet / Opus.

### Fixed

- The footage queue no longer jams: searches never wait behind analyses, more jobs run at once on strong PCs, a job
  that hangs is stopped and frees its place, jobs of a finished helper stop with it, several pieces of one video are
  downloaded once, and the chat shows the place in the queue and the expected wait.
- In Full auto (without «Ask me first») the AI no longer stops to ask you questions.
- The YouTube title, description and tags are written in the language of the video, not of the interface; the export
  dialog shows the language and lets you change it.
- An export no longer crawls at half a frame per second because of a broken footage file with no playable frames:
  Kadr checks every download, cuts a broken piece again or takes another clip, skips such a file at full speed and
  names it after the export; «Check project» finds and repairs them in older projects.
- No more single black frames at cuts (gaps shorter than a frame, photo frames fading through black, transitions into
  graphics); «Check project» finds and fixes such flashes.

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
