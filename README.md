# KCB Minerals Ledger Pro v5.0 - Premium Stable Build

This version is the high-end app package:

- Premium dashboard with live KPI cards, insights and cloud health.
- Mobile-first bottom navigation and desktop sidebar.
- Username-only login, no password.
- Google Sheet is the shared source of truth when Apps Script is connected.
- Queue-based saving: if the Sheet is temporarily offline, entries are saved locally and retried later.
- Safer transaction IDs so edits update the exact Google Sheet row.
- Edit/delete writes are verified through Apps Script JSONP responses.
- Statement quick filters: Today, 7 Days and Month.
- Search by vehicle number or distributor name.
- PWA manifest/service worker for installable app behavior.

## GitHub files
Upload/replace:

- index.html
- app.js
- style.css
- manifest.json
- service-worker.js
- assets/logo.png

## Apps Script file
Paste Code.gs into the Google Sheet Apps Script project.

Recommended: add your old Google Sheet ID here in Code.gs:

const SPREADSHEET_ID = 'YOUR_OLD_GOOGLE_SHEET_ID';

Deploy settings:

- Deploy > Manage deployments > Edit > New version
- Execute as: Me
- Who has access: Anyone

Copy the /exec URL and paste it into app.js:

const DEFAULT_CLOUD_API_URL = "https://script.google.com/macros/s/DEPLOYMENT_ID/exec";

After GitHub commit, hard refresh desktop with Ctrl + Shift + R. On mobile, clear site data once or open in incognito.
