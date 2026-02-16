# Views & Navigation

## Features in detail: view modes

The card supports three view modes that can be switched using header controls.

### Month View

Traditional month grid with color-coded event blocks.

```yaml
view_mode: month
```

**Click behavior**
- Click a day to create a new event on that date
- Click an event to open details

### Week Compact View

Each day appears as a column with stacked events.

```yaml
view_mode: week-compact
week_days: [1, 2, 3, 4, 5]
```

**Click behavior**
- Click the day header to create a new event on that day
- Click an event to open details

### Week Standard (Schedule) View

Timeline layout with hourly slots and day columns.

```yaml
view_mode: week-standard
week_start_hour: 8
week_end_hour: 21
week_days: [1, 2, 3, 4, 5]
```

**Click behavior**
- Click a time slot to create an event at that time
- Click a day header to create an event for that day
- Click an event to open details

## Rolling Days Mode

Show today plus N more days:

```yaml
rolling_days_week_compact: 2  # 3 total days
rolling_days_schedule: 6      # 7 total days
```

Use this when you want a moving upcoming window instead of fixed calendar weeks.

## Rolling Weeks Mode

Show this week plus N more weeks in month mode:

```yaml
view_mode: month
rolling_weeks: 1  # 2 total weeks
```

Useful for planning windows that update daily.

## Features in detail: interaction and navigation

### Event details modal

Click an event to view:
- Event title
- Description
- Start and end time
- Location (if provided)
- Calendar badge

### Day view behavior

Click any day to:
- Create a new event (when event management is enabled)
- View all events for that day (when event management is disabled)

### Today highlight

The current day is highlighted for quick orientation.

### Navigation

- Use arrow buttons to move between month/week ranges
- Use **Today** to jump back to the current date
