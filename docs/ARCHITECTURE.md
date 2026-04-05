# Architecture

## Overview
SMD Booking uses a simple 3-part architecture:

1. **Frontend**
   - Hosted on GitHub Pages
   - Entry point: `index.html`
   - Main app file: `smd_booking_v5_1_FINAL.html`

2. **Backend**
   - Google Apps Script Web App
   - Handles `GET` for reading bookings and `POST` for add/delete actions

3. **Database**
   - Google Sheet
   - Tabs:
     - `Users`
     - `Objects`
     - `Vehicles`
     - `Entries`

## Frontend responsibilities
- Render desktop and mobile calendar views
- Load entries from Apps Script API
- Add new bookings
- Delete bookings using `entryId`
- Map user IDs and item IDs to display names and colors

## Backend responsibilities
- Read rows from `Entries`
- Append new rows for new bookings
- Soft-delete rows by setting `active = FALSE`
- Return active rows to frontend
- Maintain `entryId` for reliable delete matching

## Data flow
1. User opens GitHub Pages app
2. App calls Apps Script `GET`
3. Apps Script reads Sheet and returns active entries
4. User adds or deletes an entry
5. App calls Apps Script `POST`
6. Apps Script updates Sheet
7. App reloads entries

## Current implementation notes
- `index.html` is only a redirect wrapper
- Most frontend logic is inside a single HTML file
- The app relies on ID mappings for users, objects, and vehicles
- Delete logic must use `entryId`
