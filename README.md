# Jaguar Suite — Fronek Skillzone Hockey

Single-file HTML apps hosted on GitHub Pages. Open `index.html` (the Home launcher) — it opens each app in its own named tab and switches between them without reloading.

| File | App |
|---|---|
| index.html | Jaguar Home launcher (also has Backup/Restore under "Data") |
| db.html | Jaguar Dev Database |
| coach.html | Coach Hours Tracker (Data Center) |
| adm.html | ADM Roster — Fall 2026 |
| ih.html | InHouse Roster — Fall 2026 |
| jaguar-backup.html | Standalone backup/restore tool — use this to pull data OUT of your old copies before switching to this site |
| drills / schedule / stats / notes .html | placeholders (coming soon) |

## Updating an app
Download the updated file from Claude, keep its name (e.g. `db.html`), drag-upload to this repo, commit. Only the changed file needs uploading — the launcher never changes.

## Data
All apps store data in browser localStorage, scoped to this site's URL, under these prefixes:
- `jaguar_` — Dev Database
- `jag_` — Coach Data Center + shared attendance/plan data
- `rm_` — InHouse Roster
- `adm_` — ADM Roster

**Moving data from your old (non-GitHub) copies to this site:** open `jaguar-backup.html` from the *same location* your old apps currently run (same folder/file path — data is tied to where the HTML loads from), click **Download Backup**, then on this new site open Home → Data → **Restore Data** and pick that file.

**Ongoing backups:** once you're on this site, just use the Data section on the Home page (`index.html`) — no need for the standalone tool anymore, though it still works if you prefer it.

Backups are a single `.json` file containing every suite key found in that browser. Restoring merges/overwrites matching keys only — it never touches unrelated site data.
