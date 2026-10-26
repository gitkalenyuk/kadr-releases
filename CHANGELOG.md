# Changelog

What changed in the two latest versions of Kadr. More on the official website: https://kadr.uk/

## [1.1.0] - 2026-10-26

The first stable release of Kadr 1.1 — everything from the 28 betas, checked by our testers, in one version for
Windows and macOS.

### Highlights

- **The AI edits the whole video** on your own Claude or ChatGPT subscription (or other AI providers): script,
  voice-over, footage, motion graphics, captions, music, sound effects and a quality check — you review and render.
- **Brief with genre** — pick the genre, language and length; Kadr sets the editing style, templates, graphics,
  transitions, photos vs video, repeat limits, music and captions by itself.
- **About 2,500 motion templates**, 30 editing styles, 27 channel profiles, maps with historical borders, a text
  animator and modern transitions.
- **Footage from 48 sources** with a smart queue, safe music (Kadr's own music beds, YouTube Audio Library, your
  library, Epidemic Sound), 40 voice providers and local speech recognition.
- **Your own recordings** — heavy 4K files get light preview copies, scene lists help the AI find the right moments.
- **Everything checked** — «Check project» finds and fixes black flashes, broken files, rights risks and more; exports
  name every clip that could not be shown.

### Fixed since beta.28

- Nothing new — 1.1.0 is beta.28, promoted to the stable channel after testing.

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
