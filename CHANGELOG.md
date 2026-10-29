# Changelog

What changed in the latest version of Kadr. More on the official website: https://kadr.uk/

## [1.1.8] - 2026-10-29

### New — experimental features (all OFF by default)

New tab **Settings → Experimental features**. Every feature there is off until you turn it on by hand, and Kadr works exactly as before without it.

- **Source check**: Kadr checks that every footage source still answers and downloads (a button and once a day while idle); the AI skips a source that failed twice in a row.
- **Fast YouTube**: YouTube searches and channel scans read YouTube's own pages — a search in under a second instead of 4–5, with upload dates; downloads stay on yt-dlp, which is also the fallback.
- **Source statistics**: once a day only anonymous counts per footage source (searches and downloads that worked or failed — no words, files or projects) so broken sources are fixed sooner.
- **Live data for charts**: the AI takes real figures from World Bank, Wikidata, the NBU, Steam, Open Library or TMDB and fills chart templates with them in the video's language, with the source line.
