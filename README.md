# Pocket Expense Tracker

A mobile-first, offline-first Progressive Web App. It uses plain HTML, CSS and JavaScript, IndexedDB for local persistence, Canvas for charts, and a service worker for offline caching. No external libraries or network APIs are used.

## Run locally

A service worker requires a secure context (`https://`) or `localhost`. Do not open `index.html` directly using `file://`.

With Python installed, from this folder run:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080` in a browser.

## Install on Android

1. Host the folder on an HTTPS static host (for example, GitHub Pages or another HTTPS web host), or access it from a local development server.
2. Open the URL in Chrome on Android.
3. Use the browser menu → **Install app** or **Add to Home screen**.
4. Launch Pocket from the home screen. After the first successful load, the service worker caches the app shell for offline use.

## Local data and backup

- Expenses and custom categories are stored in IndexedDB in the browser profile on this device.
- Export a JSON backup from Settings before clearing browser data or uninstalling.
- CSV export contains transaction rows for spreadsheet use.
- Clearing browser/site data may permanently erase the local database. Keep backups if the records matter.

## Notes

- Weekly reports run Monday through Sunday.
- Monthly reports use the current calendar month.
- Smart suggestions are derived from previously entered places/descriptions and their associated category, description and amount.
- This starter app has no cloud sync, login or server-side storage.
