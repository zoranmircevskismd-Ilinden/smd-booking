# Deployment Guide

## Frontend deployment
1. Edit or replace `smd_booking_v5_1_FINAL.html`
2. Ensure `index.html` exists and redirects to the main app file
3. Commit changes to `main`
4. Wait for GitHub Pages deployment
5. Test the live URL

## Backend deployment
1. Open Google Apps Script
2. Save code changes
3. Create a new deployment or update the Web App deployment
4. Copy the `/exec` URL
5. Update `API_URL` in `smd_booking_v5_1_FINAL.html` if the URL changed
6. Commit frontend changes if needed

## Recommended release flow
1. Backup current HTML and Apps Script
2. Make changes in a local working copy
3. Test against Sheet and Apps Script
4. Upload to GitHub
5. Confirm GitHub Pages success
6. Confirm add / delete work in production

## Cache note
If the live site appears unchanged, open the URL with a version query, for example:
- `?v=12`

## Verify after deploy
- Live app opens
- Data loads
- New entry gets `entryId`
- Delete sets `active = FALSE`
