# Changelog

What changed in the two latest versions of Kadr. More on the official website: https://kadr.uk/

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

## [1.1.0-beta.23] - 2026-10-24

### New

- **Improve prompt** — a «✨ Improve prompt» button next to Send in the AI chat. The AI chosen for the chat reads your
  request in a small separate request (it edits nothing) and shows how it understood it: topic, language, length,
  pace, voice, audience, structure, hook, ending, footage, graphics, music and captions, with missing points flagged.
  Then it asks 3–7 questions with ready answers (or type your own) and writes the improved request with every addition
  marked, each one switchable off. When your text and the brief disagree (say 10 minutes against 1 minute), you pick
  which wins. «Use» puts the request into the text box and updates the brief; you still send it yourself.
- **A channel profile from a competitor's channel** — Settings → AI assistant → Channel profiles → «Create from a
  competitor channel», or `/competitor <link>` in the chat. Kadr reads the channel's video list (titles, lengths, views;
  no whole videos are downloaded). It measures a few short low-resolution excerpts on your PC (pace, cuts, music,
  captions, faces, words per minute) and deletes them right after. The AI then drafts an editing style and a channel
  profile with a default brief, structure, hook and title rules in its own words, and a thumbnail style. Nothing is
  saved until you press Save. The competitor's name goes on the profile's banned list, and the AI is told never to copy
  content, titles, thumbnails, logos, intros or voices.
- **Reply to part of an answer** — select text in an AI answer and press «↩ Reply». It goes into the text box as a
  quote, ready for your reply, also while the AI is working.
- **YouTube description template in the channel profile** — choose the parts of the description and their order:
  title, description, chapters, tags, hashtags, credits, and your own text blocks with {title}, {channel}, {date},
  {duration}, {chapters} and {credits} (for example a fair-use paragraph). Add fixed tags that always come first,
  hashtags, and how many title and description options to make. Credits can be moved but never removed. Projects
  without a profile use the default template in Settings → Export.
- **Write with AI** — in the export dialog's YouTube section and in Recent exports, the chat's AI writes title and
  description options, tags and keywords from the script, chapters and the profile's rules. It uses your subscription
  limits or API spending like any other AI request. An optional switch in the template writes it after every export.
- **Template folders** — My templates → Folders saves folders with your own templates (for example a big DaVinci
  Resolve collection), each with a licence label: my own, free, Envato Elements, Motion Array or other paid. Their
  templates appear in the DaVinci picker. When nothing in the library fits, the AI searches them and imports only the
  one template it needs. «Import a folder…» now sits next to the Import button.
- **Timeline scrolling setting** — testers on Mac trackpads could not scroll the tracks. Settings → Keyboard & mouse →
  Timeline scrolling: «Classic (trackpad)» (up and down scroll the tracks) or «Always sideways». The default is Classic
  on macOS and Always sideways on Windows.
- **Layouts of new templates** — Settings → AI assistant: by default the AI builds and checks a new template only in
  the project's format, not in all four. Choose «All 4 formats» to get every layout.
- **Kadr finishes long jobs** — testers saw the AI stop after every step of a long job. The AI is now told to finish
  the whole request in one go. In Full auto, when a turn ends while the job is clearly unfinished, Kadr continues it
  by itself (up to 3 times per message by default), shown as «Kadr continued by itself (1/3)» with a Stop button. Switch
  it off in Settings → AI assistant → Long tasks.
- **Required updates** — Kadr can now tell you when an update is required: a banner on Home, a badge in the title bar,
  a dialog once per launch and a daily notification, each with the days left. After that date only updating works,
  and work that is already running finishes first.
- **The AI chat in a bug report** — an opt-in tick box adds the last turns of the AI chat: mode, AI, how the turn
  ended, the last actions and the final answer. Your own messages are never included, and your user name is removed from file paths.

### Improved

- **Licence colours** — Settings → Licence shows a green tick and the days left in a coloured pill. The Home
  «Subscription» block is clearly green, orange or red in every theme, and its tooltip explains the colours (testers
  could not see them in light themes).
- **«Refresh» in Settings → AI assistant** — in Models & order and in Shown in the picker, Refresh now really detects
  agents, keys and local servers again, shows a spinner and says what changed. Models & order also reloads the model
  lists and names the new models.
- **Calls the AI corrects itself are no longer red** — when Kadr refuses a malformed AI call before running it, the
  chat shows a grey row «Not run — wrong parameter, the AI is fixing it». It turns into «Fixed by the AI», or amber
  «The AI couldn't form this call» when the AI never managed. Real errors stay red.
- **The status line while the AI works** — «Starting the agent…» no longer comes back after every action. The bar
  shows what the AI is doing, how long it has been thinking, or how many helpers are working.
- **Tags are never empty** — the `.youtube.txt` file always has tags: your fixed tags, your keywords or the AI's, and
  words picked from the title, chapters, graphics and narration. The dialog says when the description is empty, the
  Preview uses this export's own file metadata, and «Copy tags» copies them. The description's credits list only the attributions; the full report stays in
  `<video>.credits.txt`.
- **Curves and rounded shapes in AI templates** — open arcs and curves keep their fill, and the AI gets tested examples
  and error messages that say what to write instead.
- **Template imports** — folders are searched deeper (up to 12 levels), files over the limit are listed instead of
  dropped, templates imported before are skipped instead of being copied again as «_2», and each template keeps its
  folder's licence.
- **Durations in your language** — run times, the live log, limits, the profile editor, the timeline and the rest of
  the window show times with the interface language's units («64 хв 53 с» instead of «64m 53s»).
- **Crash log entries are dated** — bug reports mark crashes from older versions, so an old crash no longer looks new.
- **New licence server address** — Kadr now connects to api.kadr.uk, and uses the old address when the new one cannot
  be reached.

### Fixed

- **Kadr closed itself every ~10 minutes** for some testers: a damaged subscription-limits file made it crash at every
  automatic check. The file is now repaired on start, a bad reading can no longer close Kadr, and a stuck quit no longer
  leaves a hidden Kadr running.
- **«Disconnect» for Epidemic Sound did nothing on macOS**, and neither did deleting a custom theme. Kadr now asks with
  its own confirmation dialog everywhere.
- **Copy buttons in the AI chat did nothing on macOS** — every copy now goes through the app's clipboard.
- **Pixabay and Pexels switched themselves on** — the AI can no longer switch footage sources on or off, and sources
  you marked «Skip» are never searched by the AI. Phrases such as «стоки не бери, тільки ютуб» are now understood in
  Ukrainian, Russian and English: stock is banned, YouTube stays allowed.
