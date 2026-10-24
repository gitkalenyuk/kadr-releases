# Changelog

What changed in the two latest versions of Kadr. More on the official website: https://kadr.uk/

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

## [1.1.0-beta.24] - 2026-10-24

### New

- **Fit the whole timeline and back** — press Shift+Z or `\` (or the toolbar's «Zoom to fit» button) to see the
  whole project at once, and press it again to go back to the zoom you had: to the exact same place when the playhead
  did not move, otherwise around the new playhead. The button is highlighted while «back» is available. You can move
  the key to any other one (for example Q) in Settings → Keyboard & mouse.
- **Home / End** move the playhead to the start / end of the project, and the view follows. Frame steps and other
  keyboard moves while paused now keep the playhead in view.
- **Continue in a new session** — when a CLI agent (Codex, Claude Code…) keeps failing on a long chat (for example
  Codex's `{"detail":"Bad Request"}`), the Continue strip now also offers «Continue in a new session». It starts a fresh
  session of the same AI with Kadr's recap of the chat, which always keeps your first request, the brief and the
  latest actions and results.
- **Interrupted footage downloads ask first** — after a restart, footage downloads that were cut off no longer start
  again by themselves. A card on Home says «N footage downloads from “Project” were interrupted» with Continue and
  Cancel; it goes away by itself after 24 hours.

### Improved

- **Footage work on Home** — each footage job is shown under its project with its real kind and progress («Analysing
  footage 3 of 7», «Downloading…», «Finding scenes…»), the clip title in the tooltip and a ✕ to stop it. The project
  row has «Stop background downloads», and a click opens the project's footage jobs.
- **Footage stops with the AI** — when an AI run ends or you press Stop, the footage analyses and downloads it started
  stop too (clips already downloaded are still added).
- **Lighter on the PC** — footage analysis and downloads run at background priority with fewer threads, at most 2
  analyses and 3 footage jobs at once, so a long AI job no longer freezes the computer.
- **One error card per failure** — a single agent failure used to show three identical cards; now there is one, with
  the hint.
- **The export folder button** opens the folder picker at the project's Exports folder (it is created when needed);
  any other missing folder opens at its nearest existing parent. A real error now shows a message instead of nothing.

### Fixed

- The folder button in the export dialog did nothing on Windows until the first export of a project.
- Footage downloads started by the AI kept running after the chat ended, appeared on Home as unknown downloads
  without a project or a way to stop them, and came back after every restart.
- A footage job with one clip showed 100 % while it was still being analysed.
- Errors of the window's runtime now reach Kadr's log and bug reports.
