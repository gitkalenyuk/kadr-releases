# Changelog

What changed in the latest version of Kadr. More on the official website: https://kadr.uk/

## [1.1.13] - 2026-11-09

### Added

- Updates ask first: when a new version is ready, Kadr asks «Install now», «Later» or «When everything finishes». Without an answer it installs only when nothing is running and nobody has used the PC for 15 minutes (switch in Settings → Updates). After the update Kadr reopens the project and the AI chat, and chats, downloads and «after all» continue by themselves. Only a required update past its deadline installs without asking.
- Exports next to your voiceover: when a project's voiceover is your own audio file, the finished video is saved in that file's folder (Settings → Export, on by default; files from your music folders don't count).
- Experimental, off by default: control Kadr from Telegram through your own bot (Settings → Experimental features → Telegram bot): write to the AI, start projects, see what is running, start an export and get a message with frames, answer the AI's questions with buttons, send a script as .txt / .md / .docx. Deleting and paid actions always ask for confirmation.

### Fixed

- YouTube's bot check: the chat shows a card with «Turn on cookies» (Settings → Footage → Cookies) instead of only saying YouTube blocks downloads. Kadr never bypasses the check.
- PeerTube servers that don't answer are left out of searches for a few hours, and their clips are skipped at once instead of after long timeouts.
- Several AI chats share video analysis fairly; time spent waiting for other chats no longer counts toward the analysis limit, and analyses of many videos get more time.
- The Inspector no longer closes with an error on a map place the AI named only by its name.
