# SMD Booking

SMD Booking is a lightweight web app for booking shared objects and vehicles across multiple phones with synchronized data.

## Live app
- Live URL: `https://zoranmircevskismd-ilinden.github.io/smd-booking/`
- GitHub Pages entry file: `index.html`
- Main frontend app: `smd_booking_v5_1_FINAL.html`
- Data backend: Google Apps Script Web App
- Database: Google Sheet

## Current architecture
- Frontend hosting: GitHub Pages
- Entry point: `index.html`
- Main app file: `smd_booking_v5_1_FINAL.html`
- PWA manifest: `manifest.json`
- Home screen icon: `icon.svg`
- Backend: Google Apps Script Web App API
- Data source: Google Sheet with tabs `Users`, `Objects`, `Vehicles`, `Entries`

## Main features
- View bookings in desktop and mobile calendar layout
- Add bookings
- Delete bookings
- Sync data across devices
- Support both objects and vehicles
- Uses `entryId` for reliable deletion
- Can be added to a phone home screen

## Files in this repo
- `index.html` - GitHub Pages entry shell
- `smd_booking_v5_1_FINAL.html` - main frontend app
- `manifest.json` - PWA manifest
- `icon.svg` - home screen icon
- `docs/ARCHITECTURE.md`
- `docs/CONFIG.md`
- `docs/DATA_MODEL.md`
- `docs/DEPLOYMENT.md`
- `docs/TESTING.md`
- `docs/TROUBLESHOOTING.md`
- `docs/CHANGELOG.md`
- `docs/BACKUP_AND_RECOVERY.md`
- `docs/ROADMAP.md`

## Quick update flow
1. Update Apps Script if backend changes are needed.
2. Deploy a new Apps Script Web App version if required.
3. Update `API_URL` inside `smd_booking_v5_1_FINAL.html` if the Apps Script URL changes.
4. Upload or edit `smd_booking_v5_1_FINAL.html` in GitHub.
5. Update `index.html`, `manifest.json`, or `icon.svg` if entry or install behavior changes.
6. Confirm GitHub Pages deploy succeeded.
7. Test add / delete / sync.
8. If needed, use a version query like `?v=2` to bypass phone cache before adding to home screen again.

## Important note
The main frontend logic is currently inside one HTML file. For future work, document every important change in `docs/CHANGELOG.md` and keep backups before large edits.
