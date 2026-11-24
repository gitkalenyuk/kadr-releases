# Changelog

What changed in the latest version of Kadr. More on the official website: https://kadr.uk/

## [1.2.3] - 2026-11-24

### Added

- Long videos in parts: the brief's «Length» is now a slider (seconds to hours) with «Split into parts» — minutes per part and how many AI agents work at once. The AI prepares the script, narration and style first, then every agent edits only its own part (the one that finishes takes the next), and one agent checks the whole video at the end and adds the sound, music and captions for all of it.
- Clean found footage: Kadr finds other channels' text in found videos (logos, tickers, lower thirds, subtitles, clocks), follows it as it moves, zooms in slightly, crops it out, strongly blurs what is left or puts a text-heavy clip into a frame template with your own caption, then checks again — the AI can't export while foreign text is still readable. On by default for the AI (Settings → Footage); by hand: right-click a clip → «Clean found footage».
- Expand any panel to the whole window — library, player, inspector, timeline or the AI chat: the button in its corner, a double-click on its header or Ctrl+Shift+F; Esc brings it back.

### Fixed

- Pop-ups no longer jump or close while you drag their sliders (the brief's template shares, anchored graphics and others).
- The AI panel's edge can be grabbed and dragged again; double-click returns its usual width. Every panel divider is easier to catch.
- The «Big job» estimate card can be closed (its ✕ was pushed off the panel) and stays closed for the chat.
- The timeline toolbar no longer pushes «Hide timeline» out of the window when the AI panel is docked.

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
