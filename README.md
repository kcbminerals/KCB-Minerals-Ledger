# KCB Minerals Ledger v4.8 - Sync + Edit Fix

This version keeps the no-password login but fixes two Google Sheet issues:

1. Mobile and desktop read the same Google Sheet data after sync.
2. Edited log entries update the existing row in Google Sheets instead of only changing this device.

## Files to upload to GitHub

Upload/replace these files in your GitHub Pages repository:

- index.html
- app.js
- style.css
- assets/logo.png

## File to paste in Apps Script

Paste Code.gs into the Google Sheet's Apps Script project, then deploy a new Web App version.

Important: if Apps Script is not bound to your old Google Sheet, paste your old Sheet ID in this line inside Code.gs:

const SPREADSHEET_ID = '';

Example:

const SPREADSHEET_ID = 'YOUR_OLD_GOOGLE_SHEET_ID_HERE';

## Deploy settings

Deploy > Manage deployments > Edit > New version

- Execute as: Me
- Who has access: Anyone

Copy the /exec URL and paste it into app.js at the top:

const DEFAULT_CLOUD_API_URL = "YOUR_APPS_SCRIPT_EXEC_URL";

Then commit app.js to GitHub and hard refresh the website.
