<p align="center">
  <!-- ⚠️ MISSING: Project logo (recommended 120x120px PNG with transparent background) -->
</p>

<h1 align="center">Tautulli → Letterboxd</h1>

<p align="center">
  Export your Plex movie watch history from Tautulli as a CSV file ready to import into Letterboxd — single HTML file, no install, no dependencies.
</p>

<p align="center">
  <a href="https://github.com/macokay/tautulli-letterboxd/releases">
    <img src="https://img.shields.io/github/v/release/macokay/tautulli-letterboxd" alt="GitHub release" />
  </a>
  <img src="https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/Vanilla%20JS-F7DF1E?logo=javascript&logoColor=black" alt="Vanilla JS" />
  <a href="https://github.com/macokay/tautulli-letterboxd/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-Non--Commercial-blue.svg" alt="License" />
  </a>
</p>

<p align="center">
  <a href="https://www.buymeacoffee.com/macokay">
    <img src="https://img.shields.io/badge/Buy%20Me%20A%20Coffee-%23FFDD00.svg?logo=buy-me-a-coffee&logoColor=black" alt="Buy Me A Coffee" />
  </a>
</p>

---

## Features

- **One-click CSV export** — generates a Letterboxd-compatible CSV (`Title`, `Year`, `WatchedDate`)
- **User selection** — pick any Plex user from your Tautulli instance
- **Date range filtering** — export everything or just a specific period
- **Duplicate removal** — automatically removes same-day duplicates; optional toggle to keep only the first watch of each film
- **Fully client-side** — runs entirely in your browser; your API key never leaves your machine
- **Zero dependencies** — a single HTML file, no build tools, no frameworks

---

## Requirements

| Requirement | Details |
|---|---|
| Browser | Any modern browser |
| Tautulli | Running instance with API access enabled |

---

## Installation

### Automatic

1. Download the latest `tautulli-html.html` from [GitHub Releases](https://github.com/macokay/tautulli-letterboxd/releases).
2. Open the file in any modern browser.

### Manual

```bash
git clone https://github.com/macokay/tautulli-letterboxd.git
```

Open `tautulli-html.html` directly in your browser.

---

## Configuration

On first use, enter the required fields in the settings area:

| Field | Description |
|---|---|
| Tautulli URL | Address of your Tautulli instance (e.g. `http://192.168.1.10:8181`) |
| API key | Found in Tautulli → Settings → Web Interface → API key |

Your browser must be able to reach the Tautulli URL directly. If Tautulli is on a local network, open the HTML file from the same network.

---

## Data

### Sources

| Source | Usage |
|---|---|
| [Tautulli](https://tautulli.com) | Movie watch history via `get_history` endpoint (`media_type=movie`) |

### Output

Generates a CSV file compatible with [Letterboxd import](https://letterboxd.com/about/importing-data/):

| Column | Description |
|---|---|
| `Title` | Movie title as recorded by Plex |
| `Year` | Release year |
| `WatchedDate` | Date watched in `YYYY-MM-DD` format |

---

## Updating

Download the latest release from [GitHub Releases](https://github.com/macokay/tautulli-letterboxd/releases) and replace the existing file.

---

## Known Limitations

- **Movies only** — TV shows and other media types are not exported
- **No ratings or reviews** — Tautulli does not store this data
- **Title matching** — Letterboxd matches by title and year; mismatches may occur for foreign-language or alternate titles
- **CORS / network** — the browser must reach Tautulli directly; ensure CORS headers allow the request if behind a reverse proxy

---

## Credits

- [Tautulli](https://tautulli.com/) — Plex monitoring tool providing the watch history API
- [Letterboxd](https://letterboxd.com/) — social film platform accepting the CSV import

---

## License

&copy; 2026 Mac O Kay. Free to use and modify for personal, non-commercial use. Attribution appreciated if you share or build upon this work. Commercial use is not permitted.
