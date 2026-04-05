# Data Model

## Users tab
Expected columns:
- `id`
- `name`
- `shortName`
- `active`

## Objects tab
Expected columns:
- `id`
- `name`
- `shortName`
- `color`
- `active`

## Vehicles tab
Expected columns:
- `id`
- `name`
- `shortName`
- `color`
- `active`

## Entries tab
Expected columns:
- `createdAt`
- `userId`
- `type`
- `itemId`
- `from`
- `to`
- `note`
- `active`
- `entryId`

## Meaning of Entries fields
- `createdAt` = timestamp when the row was created
- `userId` = user identifier such as `u1`
- `type` = `object` or `vehicle`
- `itemId` = object or vehicle ID
- `from` = booking start date
- `to` = booking end date
- `note` = optional note
- `active` = TRUE/FALSE visibility flag
- `entryId` = unique booking identifier used for delete

## Rules
- `entryId` should be unique
- Deleted bookings should be soft-deleted using `active = FALSE`
- Frontend should not rely on row number for delete
