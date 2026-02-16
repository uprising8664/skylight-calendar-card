# Event Management

## Enable event management

```yaml
enable_event_management: true
readonly_calendars:
  - calendar.holidays
```

- Create events from day/time slots
- View event details in popup
- Edit/delete support depends on the calendar integration

## Important integration note

Some integrations (notably Google Calendar in Home Assistant) have limitations for editing/deleting through Home Assistant APIs. If edit/delete actions are unavailable, use the integration's native app/site.
