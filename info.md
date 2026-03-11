# Info

## What You Get

A single HTML file that turns your Tautulli watch history into a Letterboxd-compatible CSV.

After running the tool you'll have a file called `letterboxd_import.csv` containing:

| Column        | Example          | Description                     |
|---------------|------------------|---------------------------------|
| `Title`       | Interstellar     | Movie title from Plex           |
| `Year`        | 2014             | Release year                    |
| `WatchedDate` | 2024-08-15       | Date you watched it (YYYY-MM-DD)|

Upload this file at https://letterboxd.com/import/ and Letterboxd will add the films to your diary.

## Requirements

- **Tautulli** running and accessible from your browser (local network or remote)
- **Tautulli API key** (Settings → Web Interface → API key)
- A **modern browser** (Chrome, Firefox, Safari, Edge — anything from the last few years)
- A **Letterboxd account** (free or paid) to import the CSV

No server, no Node.js, no Python, no Docker — just a browser.

## Getting Started

1. **Open the file** — double-click `tautulli-html.html` or drag it into your browser.
2. **Connect** — enter your Tautulli URL and API key, then click **Connect to Tautulli**.
3. **Select a user** — pick the Plex user whose history you want to export.
4. **Set dates** *(optional)* — narrow the export to a specific date range, or leave blank for everything.
5. **Export** — click **Fetch & Export CSV**. The file downloads automatically.
6. **Import** — go to https://letterboxd.com/import/, upload `letterboxd_import.csv`, and confirm.

> **Tip:** Check the *"Remove re-watches"* box if you only want each film to appear once in the export.
