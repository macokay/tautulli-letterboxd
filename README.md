# 🎬 Tautulli → Letterboxd

Export your Plex movie watch history from [Tautulli](https://tautulli.com/) as a CSV file ready to import into [Letterboxd](https://letterboxd.com/import/).

A single-page browser tool — no server, no install, no dependencies. Just open the HTML file and go.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/Vanilla%20JS-F7DF1E?style=flat&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-Non--Commercial-blue)

---

## Features

- **One-click CSV export** — generates a Letterboxd-compatible CSV (`Title`, `Year`, `WatchedDate`)
- **User selection** — pick any Plex user from your Tautulli instance
- **Date range filtering** — export everything or just a specific period
- **Duplicate removal** — automatically removes same-day duplicates; optional toggle to keep only the first watch of each film
- **Fully client-side** — runs entirely in your browser; your API key never leaves your machine
- **Zero dependencies** — a single HTML file, no build tools, no frameworks

## Installation

1. Download or clone this repository:
   ```bash
   git clone https://github.com/macokay/tautulli-letterboxd.git
   ```
2. Open `tautulli-html.html` in any modern browser.

That's it — nothing to install or build.

## Configuration

The tool connects to your Tautulli instance at runtime. You'll need:

| Setting       | Where to find it                                              |
|---------------|---------------------------------------------------------------|
| **Tautulli URL** | The address you use to access Tautulli (e.g. `http://192.168.1.10:8181`) |
| **API key**      | Tautulli → Settings → Web Interface → API key                |

> **Note:** Your browser must be able to reach the Tautulli URL. If Tautulli runs on a local network, open the HTML file from the same network.

## Data Source

All data comes from the [Tautulli API](https://github.com/Tautulli/Tautulli/wiki/Tautulli-API-Reference) (`get_history` endpoint with `media_type=movie`). Tautulli itself reads from your Plex Media Server's watch history.

The exported CSV follows the Letterboxd import specification:
- **Title** — movie title as recorded by Plex
- **Year** — release year
- **WatchedDate** — date watched in `YYYY-MM-DD` format

For details on what Letterboxd accepts, see: https://letterboxd.com/about/importing-data/

## Known Limitations

- **Movies only** — TV shows, specials, and other media types are not exported.
- **No ratings or reviews** — Letterboxd supports `Rating10` and `Review` columns, but Tautulli does not store this data.
- **Title matching** — Letterboxd matches imports by title and year. If Plex has a different title (e.g. foreign-language title or alternate spelling), the match may fail or be incorrect.
- **Large libraries** — very large watch histories (10,000+ entries) may take a moment to fetch depending on your Tautulli instance.
- **CORS / network** — the browser must be able to reach Tautulli directly. If Tautulli is behind a reverse proxy, ensure CORS headers allow the request or open the HTML file from the same origin.

## Credits

- [Tautulli](https://tautulli.com/) — the Plex monitoring tool that provides the API
- [Letterboxd](https://letterboxd.com/) — the social film platform that accepts the CSV import

## License

© 2026 Mac O Kay

Free to use and modify for personal, non-commercial use.
Credit appreciated if you share or build upon this work.
Commercial use is not permitted.
