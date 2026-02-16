# Troubleshooting

## Events are not showing

1. Confirm entity IDs are correct
2. Confirm calendars actually have events in the shown range
3. Check Home Assistant logs for calendar errors

## Cannot create/edit/delete

1. Ensure `enable_event_management: true`
2. Ensure calendar is not listed in `readonly_calendars`
3. Verify your integration supports write operations
4. Check logs for service/API errors

## Card is not loading

1. Clear browser cache
2. Confirm Lovelace resource URL is correct
3. Open browser console for frontend errors
