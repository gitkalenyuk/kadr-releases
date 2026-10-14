# Changelog

All notable changes to Kadr are documented in this file.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and Kadr uses
[Semantic Versioning](https://semver.org/). Versions with a suffix such as `-beta.1` are pre-releases and are
delivered through the **Beta** update channel.

## [1.1.0-beta.3] - 2026-10-14

### New

- **Updates without an access token.** "Check for updates" now works for everyone with an active Kadr licence: Kadr
  asks the licence server, which hands out the signed release — no GitHub token needed. Kadr still checks the
  signature of every update itself. (Install this version once by hand; after that the update button just works.)
- **macOS updates itself.** Kadr for Mac downloads the new version, checks it, swaps Kadr.app after it quits and opens
  again — no more dragging a new DMG into Applications.
- Everything from 1.1.0-beta.2 (12 interface languages, Parakeet speech recognition, smooth timeline playback,
  My voices, OpenSpeaker, the AI chat brief, 27 channel profiles, Epidemic Sound and your music library, referrals).

## [1.1.0-beta.2] - 2026-10-14

Kadr now speaks your language, plays the timeline smoothly, recognises speech faster and more accurately, and the AI
assistant is easier to steer and to switch.

### New

- **Interface in 12 languages**: English, Ukrainian, German, French, Spanish, Italian, Portuguese (Brazil), Polish,
  Dutch, Czech, Romanian and Swedish. Kadr starts in your system's language; change it in Settings → Language (the
  window reloads and your project stays open). Names of library items and messages from the engine are still English.
- **Parakeet speech recognition.** A new local model (NVIDIA Parakeet TDT 0.6B v3, 25 European languages incl.
  Ukrainian, ~640 MB, downloaded on demand in Settings → Speech to text) for captions, transcripts and dictation.
  On real Ukrainian speech it made fewer mistakes than Whisper large-v3 and runs faster — on the processor, no NVIDIA
  card or Python needed. Once installed it is used automatically for its languages; Whisper stays for the others.
- **My voices.** Voices you designed or cloned at your provider (MiniMax, ElevenLabs, Cartesia, Fish Audio, Speechify,
  Inworld) appear on their own under "My voices", and **Add voice by ID** works for every provider — the voice shows
  up in every voice menu and for the AI assistant. MiniMax keys from mainland China are detected automatically.
- **OpenSpeaker voices.** A new voice provider: one key for ElevenLabs, MiniMax, Edge, Kokoro, Vbee and Fish Audio
  voices plus your clones; also usable for speech to text (experimental).
- **Connect a voice provider** — a three-step guide (get the key → paste → free check) from every voice menu.
- **AI chat brief.** A new chat shows a Brief row: format (16:9, 9:16, 1:1, 4:5 …), voice, language, templates (use
  existing / create new / find online), captions, music and length. Kadr sets the format before the assistant starts;
  the rest guides the assistant for the whole chat.
- **Connect an AI** — ChatGPT (Codex), Claude, Gemini, an API key or your own endpoint, step by step from the model
  picker. When an AI hits its usage limit, the chat says so in plain words and offers "Switch to …" to continue the
  same request with another AI.
- **27 built-in channel profiles** (true crime, history, fairy tales, horror, science, news, tech reviews, podcast clips,
  gaming, sports, travel, cooking, fitness, beauty, product ads, weddings …) with detailed editing rules for the
  assistant — graphic system, captions, pacing, format, transitions, music; use one as is or duplicate and edit it.
- **Music: Epidemic Sound and your own library.** Library → Audio → Music searches your Epidemic Sound subscription
  (paste a key from epidemicsound.com → Account → API keys in Settings → Music), adds tracks or just their
  instruments / drums / bass stems under narration, and credits them after export. Add folders of tracks you already
  downloaded and Kadr indexes them (tags, length, BPM on request). The AI assistant picks music from both.
- **Referral programme.** Settings → Licence shows your referral code; every friend who activates Kadr with it adds
  days to your access (and gives them a welcome bonus).
- The chat panel is wider and can be resized; the message box is taller.
- Custom AI providers: **Load models** fetches the model list from your server; model ids are no longer required.

### Fixed

- **Timeline playback**: sound played as garbled noise — it is now clean and in sync. Clicking the ruler shows the
  frame almost at once, dragging the playhead shows frames while you drag, and playback no longer stutters on archive
  footage inside templates.
- Export: the folder button opens a folder picker.

## [1.1.0-beta.1] - 2026-10-13

The biggest update since 1.0: motion-graphics templates with a layer editor, a built-in AI assistant that edits for
you, voices and AI video from dozens of providers, a footage finder, local analysis of beats, shots and faces — and,
from this version on, **Kadr is activated with a personal code**.

### Activation (read this first)

- **Kadr now needs an activation code.** On the first start after this update Kadr shows an activation screen: type
  the code you received from the owner of Kadr (`KADR-XXXX-XXXX-XXXX`) and Kadr unlocks at once. A code works on one PC.
  Your projects stay on your computer and are never touched — without a valid licence Kadr simply does not open them.
- **Access for a set time.** Your access may have an end date; the title bar shows a badge in the last three days and
  Settings → Licence shows the details (until when, which features, this PC's id). Ask the owner to extend it.
- **Works offline for three days.** Kadr checks your access in the background when it starts and every few hours. It
  keeps working without internet until its last check is three days old.
- **The owner can close access at any time** — an online Kadr stops within a second; projects stay on disk.
- `kadrctl`, `kadr-mcp`, the REST API and the built-in assistant obey the same licence. `license.status` tells why
  Kadr is locked; activation is done by you, never by AI agents.

### New

- **Motion graphics.** 690 ready templates in 18 graphic systems — titles, lower thirds, captions, call-outs, counters,
  charts, maps, social cards, transitions and overlays — each one a single clip on the timeline with its own fields,
  media slots, layouts for 16:9, 9:16, 1:1 and 4:5, and sound cues. A layer editor (keyframes, easing curves, solo,
  per-ratio layouts) opens in place of the timeline; project styles and brand kits restyle every template at once.
  Import your own templates from DaVinci Resolve / Fusion (`.setting`, `.comp`, `.drfx`) and Lottie, or let the
  template finder look for free ones online.
- **Animated maps** — offline, with historical borders from 3400 BC to today, towns, rivers and lakes, routes, pins and
  a camera that flies between places.
- **Text animator.** Per-letter, per-word and per-line animations with full control over timing and easing.
- **A modern library.** 40 new transitions, 39 effects and 45 clip animations; dated items are hidden from the library
  (your old projects still render exactly as before). New 4:5 canvas.
- **Built-in AI assistant** (the "AI" button, Ctrl+Shift+A). Chat with Claude Code, Codex, Gemini CLI and a dozen other
  agents, or with Anthropic, OpenAI, Gemini and other APIs, and it edits your project like a person would — every step
  undoable, a checkpoint to revert the whole chat. It follows an editing playbook, checks its own work (`qa.check`
  looks at real frames), assembles rough cuts on the beat, renders thumbnails and remembers your channel profiles.
  Choose how much it may do alone (up to Full auto), dictate with the microphone, continue long tasks, use your own
  API endpoints for Claude Code, and pick models, advisor and effort.
- **Voices and AI video from many providers.** 39 voice providers (ElevenLabs, OpenAI, Azure, Google, Edge read-aloud
  and more, plus local engines) and 37 AI video providers with about 1,900 models. Re-voice a clip with one click in
  Inspector → Speech; captions follow.
- **Speech to text** for dictation and transcription: local Whisper or 15 cloud services.
- **Footage finder.** Search 48 free and stock sources, preview, download and import in one step; Kadr writes a
  credits file next to every export that needs one.
- **Local analysis** on this PC, free: beats and downbeats, shot boundaries, faces and text-to-picture relevance
  (models download on demand).
- **Keys stay safe.** API keys live in an encrypted vault (Windows protects it for your account), several keys per
  provider with automatic failover, and a daily spending limit with a ledger of every paid call.
- **Sound.** Every mix ends in a true-peak limiter, and export can normalise loudness (e.g. −14 LUFS for YouTube).
- WebM clips with transparency (VP8/VP9 alpha) keep their alpha.

### Fixed

- An export that ran out of video memory now goes back to the graphics card instead of finishing on the processor.
- A rare graphics-driver hang on very complex graphics: Kadr now splits heavy GPU work, watches the driver and falls
  back to the processor instead of freezing.
- FFmpeg installed with Scoop is found and started correctly.
- Home shows a real frame of each project on its card.

## [1.0.0] - 2026-10-06

Kadr is out of beta. Everything you see — every clip, photo, filter, effect, transition, animation and title — is now
drawn on the graphics card, so exports finish in a fraction of the time and the processor stays free.

### New

- **GPU rendering on NVIDIA, AMD, Intel and Apple Silicon.** The player, frame previews, contact sheets and export are
  composited on the graphics card: transforms, crops, masks, chroma key, every blend mode, all 227 filters and LUTs,
  the Adjust tab, grain and vignette, all 195 video effects, all 221 transitions, all clip animations, and text with
  every style and letter animation. Kadr uses Vulkan or Direct3D 12 on Windows and Metal on macOS (Apple Silicon M1–M4
  and Intel Macs). Without a usable graphics card (no driver, remote desktop, virtual machine) Kadr falls back to the
  processor automatically and the picture is the same.
- **Much faster export.** Video frames are decoded by the graphics card (NVDEC, AMF, Quick Sync, VideoToolbox),
  composited on it and handed to the hardware encoder without a round trip through the processor. Measured on an
  RTX 3060 at 1080p30: a 53-minute documentary with 541 cuts, LUT filters, grain, dust and titles exports in
  6 minutes (260 fps, 8.7× real time) instead of 46 minutes; a 1-minute project in 8 seconds instead of 50. The
  processor does about 15× less work, and the sound is mixed while the picture renders instead of before it.
- **Choose how much video memory Kadr may use.** Settings → Rendering shows each graphics card with its total memory.
  Set a limit (or leave it on Auto); Kadr always keeps a reserve free for Windows and other apps (0.5 GB by default),
  so with a 12 GB card and "12 GB" chosen it uses at most 11.5 GB. Caches, frames in flight and the number of hardware
  decoders follow the limit, and changes apply to the next frame or export without a restart. Pick the graphics card
  and the mode (Auto, GPU, CPU) in the same place, or through `render.settings.set`.
- **Configurable API port.** Settings → API changes the address the local API listens on (default
  `127.0.0.1:7777`); the app moves to the new port at once. `kadrctl`, `kadr-mcp` and the Go client find the running
  Kadr automatically through `api-endpoint.json` in the data folder, so agents keep working after a change.
  `KADR_ADDR` still overrides everything. New commands: `render.devices`, `render.settings.get`,
  `render.settings.set`, `app.api.get`, `app.api.set`; `export.status` and `app.version` report the active renderer.

### Changed

- **Version 1.0.0, out of beta.** Installed copies follow the Stable update channel by default; beta testers are
  moved from Beta to Stable unless they chose Beta themselves.
- **Distribution by invitation.** Kadr is shared privately. Installers come from the person who invited you; the
  website keeps the documentation for people and AI agents but no longer offers downloads. Automatic updates need a
  GitHub access token from the vendor (Settings → Updates, `update.settings {"github_token": "…"}` or the
  `KADR_UPDATE_TOKEN` environment variable); without one, "Check now" simply says the update channel is private.

## [0.1.0-beta.4] - 2026-10-06

Export is about four times faster, and two annoying errors are gone.

### Faster

- **Export up to ~4× faster.** A 29-minute 1080p photo documentary with colour filters, grain and Ken Burns moves
  now exports at ~45 frames per second instead of ~12. Colour filters, grain and blending run several times faster,
  big photos are resized once instead of every frame, the blurred background behind a photo is built once per clip,
  and Kadr now uses all your processor cores while exporting.
- **Video clips decode on the graphics card** (NVIDIA, Intel or AMD) when exporting HD and 4K footage, with an
  automatic fallback to the processor. Set `KADR_HWDEC=0` to turn it off.

### Fixed

- Saving a project could fail with "Access is denied" on Windows when another program briefly held the project file.
- Installing a font right after starting Kadr could fail with "The system cannot find the path specified".

## [0.1.0-beta.3] - 2026-10-02

A much bigger library — several times more transitions, effects, filters, animations, text looks, stickers and
backgrounds — animated previews when you hover a card, 24 fonts with Cyrillic out of the box and 146 more in one click.

### New

- **See it move before you add it.** Hover any card for a moment — in the Transitions, Effects, Filters, Text and
  Stickers tabs, the Animation tab, Text → Effects and Animate, the Transition, Effect and Filter panels, caption styles
  and My kit — and it plays an animated preview rendered by Kadr's engine.
- **221 transitions** (was 68) in 19 tabs, with new Wipe, Zoom, Spin, Liquid, Particles, Film, Retro and Split tabs and
  directional whip pans. 23 of the new transitions take a direction and 13 an edge softness.
- **195 video effects** (was 56) in 20 tabs, with new Motion, Frame, Stylize, Weather, Dreamy and Color tabs. Every new
  effect has 1–4 sliders of its own.
- **227 filters** (was 70) in 25 tabs, with new Cinematic, Vintage, Aesthetic, Mood, Seasons, Duotone and Special looks
  and portrait filters that keep skin tones natural.
- **310 clip animations** (was 136): 105 In, 105 Out, 53 Combo and 47 Loop — blinds, slats, hinge swings, coin spins,
  slot rolls, shine sweeps, RGB splits, motion smears, waves and more. Loops now work on videos, photos, stickers and
  text alike.
- **175 text templates** (was 46), with new Vlog, Quote, Sale, Luxury, Gaming, Love, Travel, Food, Sports, News,
  Minimal, Impact and Kinetic tabs.
- **114 word-art effects** (was 22) and new text looks in Text → Effects: 28 patterns (glitter, holographic foil,
  marble, plaid, leopard…, some of them moving), bevel and emboss, inner shadow and inner glow, echo stacks, grunge,
  chalk and stamp textures, sparkles, drips, gradient outlines, a hand-made wobble and pixel art. The background box
  can now be one box per line, slanted, bordered, shadowed, gradient-filled or cut out around the letters.
- **137 letter animations** (was 39): 55 In, 45 Out and 37 Loop, such as decrypt, split-flap, terminal cursor, jelly
  pop, rain drop, glitch and neon buzz.
- **55 caption styles** (was 15) with new Karaoke, Pop, Cinematic, Neon, Minimal, Creator and Fun tabs, and 7 new word
  highlights: pop, bounce, reveal, dim ahead, glow, underline sweep and gliding box. Box-style highlights can recolour
  the spoken word's letters.
- **394 stickers** (was 82), 73 of them animated, with new Animated, Love, Party, Nature, Food, Tech, Retro, Travel,
  Sports, 3D and Folk tabs. Animated stickers arrive with their animation already applied.
- **98 generated media presets** (was 32) from 13 new generators: mesh gradients, aurora, lava lamp, plasma, bokeh,
  particles, light leaks, film dust, textures, patterns, styled timers, banners and frames. Moving backgrounds loop
  seamlessly; banners and frames are transparent overlays; light leaks and film dust are made for the Screen blend mode.
- **Fonts.** A new font picker in Text → Basic → Font with search, style filters (Sans, Serif, Display, Handwriting,
  Monospace, Pixel), a Cyrillic filter, *My fonts* and *More fonts*: 146 free, open-licence font families (123 with
  Cyrillic) that download and apply in one click. Import your own `.ttf`/`.otf` files too. Variable fonts get real
  Regular and Bold weights. Downloaded fonts are kept in `%APPDATA%\Kadr\fonts`.
- **24 fonts included, no download needed** — all with Cyrillic: Montserrat, Rubik, Oswald, Manrope, Unbounded, Russo
  One, Rubik Mono One, Comfortaa, Yeseva One, Seymour One, Tektur, Rubik Bubbles, Caveat, Lobster, Pacifico, Marck
  Script, Amatic SC, Bad Script, Playfair Display, Lora, Prata, JetBrains Mono, Press Start 2P and Pixelify Sans
  (SIL Open Font License; listed under *Bundled*).

### Fixed

- Some valid font files (for example Pacifico, Rubik Italic and Rubik Bubbles) were rejected when installing or
  importing, and some installed system fonts were missing from the font list.
- A few pop-style clip animations showed the clip at full size for one frame at their start or end.

### For AI agents and scripts

- **`library.preview`** returns a PNG contact sheet of how a transition, effect, filter, animation, text look, caption
  style, animated sticker or generated clip plays — over MCP it arrives as an image, so an agent can look before it
  chooses. Items that move carry a `preview` field (`GET` its `url` for the JPEG sprite strip).
- **Font commands:** `font.catalog`, `font.install` (background download with `font.progress` events), `font.import`,
  `font.remove` and `font.rescan`; event `fonts.changed`; `GET /api/v1/fonts/{id}/preview`.
- New optional text style fields (`pattern`, `bevel`, `inner_shadow`, `inner_glow`, `echo`, `distress`, `sparkle`,
  `drip`, `rough`, `pixelate`, `stroke_fill`, `fill.stops`, box extras, `highlight.text_color`) in `text.add`, with
  flat parameters in `text.update`.
- `sticker.add` applies an animated sticker's animations unless `animate: false`; `media.generate` has 13 new kinds.
- 183 documented commands (was 177).

## [0.1.0-beta.2] - 2026-10-01

Second public beta. If you have 0.1.0-beta.1 installed, Kadr offers this update automatically (Settings → Updates).

### New

- **Voices settings** (Settings → Voices): paste an ElevenLabs API key to use natural cloud voices — including
  Ukrainian — for text to speech. The key stays on your computer and is sent only to ElevenLabs.
- **ElevenLabs text to speech** through the API as well: `tts.set_api_key`, then `tts.speak` / `tts.from_text` with
  voices named `elevenlabs:<voice_id>`.
- **Watch an AI agent work:** new `ui.open_project`, `ui.select`, `ui.library_tab` and `ui.toast` commands let an agent
  show what it is doing in the open window.
- **The editor takes over from the background engine:** if an AI client started a headless `kadr-server` (via
  `kadr-mcp`), opening Kadr now takes over the API port, so the agent's edits appear live in the window.
- `kadr-mcp` starts the engine on demand when Kadr is not running.
- Web mode deep link: `?project=<id>` opens a project directly.

### Fixed

- `kadrctl batch` accepts JSON files saved with a UTF-8 byte-order mark (Notepad / PowerShell).
- The portable build keeps its data in a `data` folder next to `Kadr.exe`.
- OpenAPI operations now carry `x-scope`, `x-read-only` and `x-undoable`.

## [0.1.0-beta.1] - 2026-10-01

The first public beta of Kadr. Kadr is a CapCut-style desktop video editor for Windows where every action is also an
API command, available over REST, MCP (for AI agents), the `kadrctl` CLI and WebSocket events.

> **Install notes.** The installer is not code-signed yet, so Windows SmartScreen may warn you: choose
> **More info → Run anyway**, and compare the file hash with `SHA256SUMS.txt` if you want to be sure. Kadr does not
> bundle FFmpeg. On first launch it offers to download an official GPL build, or you can point it to your own FFmpeg.
> Requires Windows 10 1809+ or Windows 11 (x64) with the WebView2 Runtime.

### Editor

- CapCut-style workspace: home screen with projects, media library, player, inspector and a multi-track timeline in
  a dark theme.
- Projects in 10 canvas ratios (16:9, 9:16, 1:1, 4:3, 3:4, 21:9, 2.35:1, 2:1, 1.85:1, 5.8-inch), any frame rate,
  canvas background (colour, blur or image), cover frame, duplicate and rename.
- Media import of video, photo, audio and animated GIF files or whole folders by button, native dialog or drag and
  drop, with duplicate detection. Thumbnails, filmstrips and waveforms are generated in the background.
  **Proxies** make 4K and HEVC footage smooth to edit, and moved files can be relinked.
- Generated media: gradients, film grain and noise, drifting shapes, countdowns, grids, checkers, stripes and test cards,
  rendered locally (9 kinds, 32 presets).
- Timeline with a magnetic main track, video overlays (picture-in-picture), text, sticker, effect, filter,
  adjustment and audio tracks, snapping, linkage, preview axis, markers with colour and label, and track
  lock, hide and mute.
- Clip tools: split (`Ctrl+B`), delete, delete left/right (`Q`/`W`), duplicate (`Ctrl+D`), replace, freeze frame,
  reverse, mirror, rotate, crop with ratio presets, copy/cut/paste (`Ctrl+C`/`Ctrl+X`/`Ctrl+V`).
- On-canvas editing: select, move, scale and rotate clips in the player with snapping guides, plus a hand tool, zoom
  presets, arrow-key nudge and safe-zone overlays for vertical video.
- Speed from 0.1× to 100× with *keep pitch*, and speed curves (montage, hero, bullet, jump cut, flash in, flash out, or
  a custom curve).
- Compositing: position, scale, rotation, opacity, 14 blend modes, 6 mask shapes with feather, rounding and invert,
  chroma key, and a canvas background per clip.
- Keyframes on 22 properties (transform, opacity, volume, 15 colour controls, filter intensity) with four easing curves.
- Undo and redo for every edit, whoever made it. *My kit* presets save text styles, colour settings, filters, effects,
  transitions and animations for reuse in every project.

### Colour

- 14 basic adjustments: brightness, contrast, saturation, exposure, temperature, tint, highlights, shadows, sharpen,
  vignette, hue, fade, grain and shine.
- HSL with 8 colour bands, tone curves (master, R, G, B; up to 16 points; 7 presets) and `.cube` LUTs with intensity.
- Auto adjust, which corrects exposure, contrast, white balance and saturation from frame analysis.
- 70 original filters in 18 categories with keyframable intensity, plus adjustment layers.
- Video denoise and deflicker.

### Text and captions

- Text with 4 built-in fonts and every installed system font (with Cyrillic and CJK fallback): stroke and extra outlines,
  shadow, background box, glow, gradient fill, 3D extrude, curved text and letter case.
- 46 text templates, 22 word-art effects and 39 per-letter/per-word text animations (typewriter, letter rise,
  karaoke sweep, scramble, word pop and more).
- **Offline auto captions** with Whisper (faster-whisper): about 100 languages plus auto-detect, word-level timing,
  model choice from `tiny` to `large-v3`, and NVIDIA GPU acceleration.
- 15 caption styles, including word highlight and karaoke looks, and a caption editor to edit, split, merge, shift
  and restyle cues.
- Subtitle import (SRT, VTT, ASS/SSA, LRC) and export (SRT, VTT, TXT, LRC).
- **Transcript-based editing:** delete words to cut the video, remove filler words (English, Ukrainian, Russian, plus
  custom words) and remove pauses.
- Local text-to-speech with Windows SAPI voices and eSpeak NG, loudness-normalised, with an option to fit the text
  clip to the speech.

### Library

All items are original and generated or rendered by Kadr's own engine:

- 68 transitions in 11 categories (including 3D cube and flip, blinds, iris shapes, ripple, swirl and zoom blur), with
  direction and softness options.
- 56 video effects in 14 categories, each with its own parameter sliders.
- 136 clip animations: 44 in, 44 out, 28 combo and 20 loop.
- 82 stickers in 14 categories, 47 synthesised sound effects in 9 categories and 25 voice effects.

### Audio

- Volume in dB with keyframes, fades, noise reduction and loudness normalisation (−14 LUFS with a true-peak limit).
- EBU R128 loudness meter and beat detection with BPM and automatic beat markers.
- Separate audio (`Ctrl+Shift+S`) into a linked audio clip, and restore it later.
- A sound-effects browser with categories, search, preview and one-click add at the playhead.

### AI and smart tools (local)

- Remove background, using `rembg`, `onnxruntime` or `torch` on your machine.
- Scene detection and *split scenes*, *remove silence*, *auto reframe* (for example 16:9 to 9:16 following the
  subject), auto adjust, and beat detection.
- `ai.capabilities` and `captions.asr_status` report which optional components are installed and how to add the rest.

### Export

- 480p to 4K, 24 to 60 fps, H.264 or HEVC in MP4 or MOV, with quality presets or a custom bitrate.
- Automatic GPU encoding (NVIDIA NVENC, Intel Quick Sync, AMD AMF) with a software fallback.
- Animated GIF, audio-only MP3, WAV, AAC and FLAC, and range export.
- Size estimate, a background export queue with progress and cancel, and *open folder*.

### API, MCP and CLI

- 160+ documented commands generated from one registry. Each has a detailed description, typed parameters with units,
  examples, and errors with hints.
- REST API on `127.0.0.1:7777` with token authentication, an OpenAPI 3.1 spec (`/api/v1/openapi.json`) and an HTML
  reference at `/docs`.
- Atomic **batches** that apply many commands as one undo step, with **dry run**.
- WebSocket events for project changes, playback, imports, exports, captions and AI jobs.
- `kadr-mcp.exe`: an MCP server for Claude Desktop, Claude Code and other MCP clients. `preview_frame` and
  `preview_contact_sheet` return images, so agents can see their edits.
- `kadrctl`: list, describe and run commands from the terminal, with human time formats (`2.5s`, `00:01:02.5`).
- `kadr-server.exe`: the headless engine for scripts and pipelines.

### Installer and updates

- Per-user installer in English and Ukrainian (no admin rights needed) with an optional all-users mode, shortcuts,
  an optional *Add kadrctl and kadr-mcp to PATH* task, a WebView2 check and an uninstaller that asks before deleting your
  projects or the downloaded FFmpeg. A portable zip is also available.
- First-run FFmpeg setup: one click downloads the official BtbN GPL build of FFmpeg 7.1 (about 100 MB, SHA-256
  verified) into `%LOCALAPPDATA%\Kadr\tools\ffmpeg\bin`, or you can point Kadr to an existing FFmpeg
  (`tools.install_ffmpeg`, `tools.set_ffmpeg_dir`).
- Automatic updates from GitHub Releases, verified with an **Ed25519-signed manifest** and the installer's
  **SHA-256**. Installs silently in place and relaunches Kadr. Stable and Beta channels (pre-release builds default to
  Beta), *skip this version*, and update commands for agents (`update.check`, `update.install`, …).
- Settings window with *About*, *Updates* and *API* sections (address, token file and docs link).

[0.1.0-beta.1]: https://github.com/gitkalenyuk/kadr/releases/tag/v0.1.0-beta.1
