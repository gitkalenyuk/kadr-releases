# Changelog

What changed in the latest version of Kadr. More on the official website: https://kadr.uk/

## [1.2.2] - 2026-11-23

### Added

- Home shows which projects wait for an export: «AI finished — not exported» / «AI stopped — not exported» badges (when, why, changed since the last export in the tooltip) and a «Not exported» filter.
- Template preview without the timeline (Library → Templates): a click plays the template full size in the player in your project's format; «+ Add» or the round «+» on the card puts it on the timeline. Dragging works as before.
- Music folders per channel (Settings → AI assistant → Channel profiles → Music folders): pin your music folders or packs to a channel, optionally with Kadr's own music; the AI takes that channel's music only from them, Check project warns about other tracks, and Library → Audio → Music has «This channel's music».
- Your own keys for sources that work without one (DigitalNZ, Imgflip) with your account's limits; every footage source shows its active limit, today's requests and what the provider reported; «Check connection» tests a key for free where the provider allows it.
- Bright Data as a paid web search next to Brave and SerpApi (estimate first, counted in the daily spending limit).
- Experimental — Apify in Live data: with your own Apify token the AI can look up Google News, Google Search, YouTube and Reddit for a video's topic; every run is estimated, capped and counted in the daily spending limit.

### Fixed

- DVIDS and NARA keys that work outside Kadr now work in Kadr (DVIDS 403, NARA answering a web page).
- Limits for AI agents (Settings → Footage) keep your values across updates and restarts, also when another Kadr process writes the settings; each limit says whether it is your value or Kadr's default.
- YouTube downloads: when Chrome locks its cookies, public videos download without them and Settings → Footage → Cookies says so; removed, private or age-gated videos and YouTube's bot check fail at once with the real reason instead of retrying for many minutes. Updating yt-dlp works while it runs.
- The AI chat with Codex no longer fails on every turn after you added Kadr's MCP to Codex's own config; a thread Codex can't resume restarts by itself with the chat's recap; a kadr-mcp removed by antivirus shows one card saying how to restore it.
- macOS: Kadr no longer closes when several AI chats analyse footage (face detection) at the same time; each local model is loaded once and shared.

## [1.2.1] - 2026-11-13

### Added

- Quick commands in the AI chat: save any message you sent with the bookmark under it (name it, edit the text), then pick it in any chat of any project from the ⚡ button next to the paperclip, the brief or by typing / and its name — the text goes into the message box, nothing is sent by itself. Edit or delete from the list; Export / Import moves them to another computer.
- Motion for stills in one click (Inspector → Animation → Motion): Ken Burns, zoom, pan, focus on a detail, punch-in, shake, drift and parallax with a strength slider — the picture always covers the frame. Arrows, circles and frames can be pinned to a point of the clip under them and follow its zoom (Graphic tab → Pin to the clip below).
- Experimental — Deep competitor analysis (Settings → Experimental features; then Channel profiles → Create from a competitor channel → Deep): 10, 15 or 20 videos, their scripts read, the most typical ones studied whole, every scene looked at by the AI. The result is a channel profile with a recipe — format, structure, kinds of inserts, sources, motion and sound — that the channel's videos follow; Check project warns when a video drifts from it.
- Experimental — Memes and GIFs: GIPHY (with your own free key) and popular Imgflip meme templates in the footage finder; the AI uses them only after you switch on «Memes for AI» in Settings → Footage, and credits them.
- Experimental — Website screenshots: a picture of any web page by its link, taken with the Edge or Chrome already on your computer, added to the project as a photo with the page address as its source (Media → the globe button).
