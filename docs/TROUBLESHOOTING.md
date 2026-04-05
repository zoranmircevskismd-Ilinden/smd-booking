# Troubleshooting

## GitHub Pages failed deploy
- Check that `index.html` exists
- Check that `index.html` is valid HTML
- Check repository Pages settings

## Live site shows old version
- Force refresh browser
- Open live URL with a version query like `?v=12`
- Confirm latest GitHub Pages deploy succeeded

## Add works but delete does not
- Confirm `entryId` exists in `Entries`
- Confirm frontend sends `entryId`
- Confirm backend uses `entryId` for delete
- Confirm `API_URL` points to the current Apps Script deployment

## New entries do not get `entryId`
- Check `addEntry()` in Apps Script
- Check that backend deployment is updated
- Check that frontend uses the current Apps Script URL

## Entries disappear only when changed manually in Sheet
- Backend read is working
- Write/delete path is not matching the same deployment or logic

## Dates look wrong
- Normalize dates in frontend and backend
- Avoid relying on raw ISO timestamps for matching deletes
