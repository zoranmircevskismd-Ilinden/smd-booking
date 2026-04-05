# Configuration

## Frontend config
Main app file: `smd_booking_v5_1_FINAL.html`

Important frontend constant:
- `API_URL` = current Google Apps Script Web App endpoint

When backend deployment URL changes, update `API_URL` inside the main HTML file.

## GitHub Pages
- Branch: `main`
- Entry point: `index.html`
- Main app file redirected from `index.html`: `smd_booking_v5_1_FINAL.html`

## Google Sheet tabs
- `Users`
- `Objects`
- `Vehicles`
- `Entries`

## Current known ID mapping
### Users
- `u1` = Zemo
- `u2` = Kole
- `u3` = Dzole
- `u4` = Bratko

### Objects
- `o1` = Skopje
- `o2` = Ohrid
- `o3` = Mavrovo
- `o4` = Greece
- `o5` = Croatia

### Vehicles
- `v1` = Vito
- `v2` = LT35

## Important behavior
- `entryId` must exist for reliable delete
- `active = TRUE` means visible booking
- `active = FALSE` means deleted / hidden booking

## Time / date handling
- Frontend displays and compares normalized `YYYY-MM-DD` dates
- Backend should normalize dates consistently
