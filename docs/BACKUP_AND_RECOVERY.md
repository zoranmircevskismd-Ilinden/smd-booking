# Backup and Recovery

## What to back up
- `smd_booking_v5_1_FINAL.html`
- Apps Script source code
- Google Sheet structure and values

## Recommended backup practice
- Before major changes, save a dated copy of the HTML file locally
- Export or copy Apps Script code into a text file
- Duplicate the Google Sheet before structural changes

## Recovery
- If frontend breaks, restore the previous working HTML file
- If backend breaks, redeploy the previous Apps Script version
- If sheet structure breaks, restore from a duplicated Sheet backup

## Do not delete without backup
- `index.html`
- main HTML app file
- `Entries` tab columns
- Apps Script deployment URL reference
