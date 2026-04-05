# Testing Checklist

## Basic checks
- App opens on GitHub Pages
- Desktop view renders
- Mobile view renders
- Plus button opens the entry sheet

## Data checks
- Existing entries load from Google Sheet
- New booking can be added
- New booking gets an `entryId`
- Deleted booking sets `active = FALSE`
- Deleted booking disappears from app after reload

## Cross-device checks
- Add on device A, verify on device B
- Delete on device B, verify on device A

## UI checks
- Multiple entries in one day display correctly
- `+ more` opens day sheet
- Delete modal opens correctly
- Date text displays in clean `YYYY-MM-DD` format

## Regression checks
- `API_URL` points to current Apps Script deployment
- `index.html` still redirects correctly
- GitHub Pages deploy succeeds
