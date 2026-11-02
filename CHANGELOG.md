# Changelog

What changed in the latest version of Kadr. More on the official website: https://kadr.uk/

## [1.1.11] - 2026-11-02

### Fixed

- Kadr AI music no longer makes noise: a wrong setting made the AI music pack generate noise-like sound; nothing to reinstall, old noisy tracks aren't reused, a noisy result is refused, and on Auto Kadr uses its own music instead.
- AI chats don't disappear after a crash: an interrupted chat opens with Continue even many hours later; older chats are always behind the history icon.
- Work continues after a crash: on Windows a chat that was running continues once by itself (this uses your limits; «Continue after a crash» in Settings → AI assistant → Long tasks turns it off), otherwise a Home card and a notification offer Continue. On Mac: the card and the notification only.
- «When everything finishes» survives a crash restart for up to 24 hours and waits until the chat continues; if the chat can't continue, the PC stays on and Kadr tells you.
- Updates finish even if Claude Code or another tool is using Kadr's MCP at that moment, and Kadr reopens afterwards.
- Steadier when memory runs short: Check project and video decoding use less memory when the PC's memory is almost full, so there should be fewer crashes; crash reports record memory use, including the names of the biggest programs, never their paths or arguments.
- Helpers get more time to look through footage on longer videos, and a look stopped before it finished no longer counts.
