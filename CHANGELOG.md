# Changelog

What changed in the latest version of Kadr. More on the official website: https://kadr.uk/

## [1.1.14] - 2026-11-10

### Added

- Claude Fable 5.2 in the model list (Anthropic API, and Claude Code 2.1.321 or newer), plus Claude Haiku 5.5.
- 383 new templates, built to look different: 112 media frames that hold your video or photos (for one to six pictures), 51 templates for true crime, finance, sports, gaming, tutorials, education and lifestyle, and five new graphic systems — Paper Cutout, Terminal, Neo-brutalist, Analog Horror and Liquid Glass.
- New footage sources without a key: The Met, Cleveland Museum of Art, Wellcome Collection, NASA Scientific Visualization Studio and Our World in Data charts. Sonniss and StreamBeats folders are recognised in My music library. Separate links for Ukrainian government and archive sites.
- The AI no longer exports a video with errors: before exporting it must run Check project on the current state and fix gaps, overlapping graphics, unreadable files and cut-off text. Your own exports are never held back, and «export anyway» in the chat lifts it.
- Cleaner cuts: the AI's rough cut no longer stretches a found clip past the part that was chosen, and Check project warns about held frames, hidden slow motion and shots that run too long.
- Experimental, off by default: Learn an editing style (Settings → Experimental features, then Settings → Learn a style) — give a YouTube link or a video file, Kadr measures its pace, cuts, captions and sound, and opens a new editing style you can change and save.
- Experimental, off by default: Repeat a video (Settings → Experimental features) — drop a video or a link in the AI chat, Kadr studies its structure and shows a blueprint you can edit; after «Build» the AI makes a new video with its own script, footage, templates and music. The original is never used as material, and the result is checked against it before export.
- Telegram bot (experimental): a menu with buttons, a project browser, a live progress message for the running AI task, export presets, voice messages (recognised on your PC), photos and videos into the project, Check project with Fix buttons, limits, scheduled edits, a PIN and auto-lock, and switches for what may be sent to Telegram. By default an AI task driven from Telegram asks before risky actions (Settings → Telegram).

### Changed

- Lighter on the PC: downloads at once follow the PC's power (4, 6 or 10), Kadr reacts to low memory on macOS too, and helpers default to 3 on smaller PCs.
- The Templates tab and long AI chats are much faster.

### Fixed

- «Skip this version» now really stops the automatic install of that version.
- Putting the PC to sleep no longer cancels footage analysis, and a short network drop no longer switches working sources off for hours.
- The rough cut's «fade» and «dissolve» transitions are placed instead of being silently dropped.
- Telegram bot: a message is never run twice after a restart, /stop is read while a long action runs, and the pairing code is not shown to AI agents.
