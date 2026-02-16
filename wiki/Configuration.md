# Configuration

## Minimal working config

```yaml
type: custom:skylight-calendar-card
title: Family Calendar
entities:
  - calendar.family
```

## Common options

```yaml
type: custom:skylight-calendar-card
title: Family Calendar
entities:
  - calendar.personal
  - calendar.work
  - calendar.family
view_mode: month
default_view: week-standard
first_day_of_week: 0
show_week_numbers: false
compact_header: false
colors:
  calendar.personal: '#FF6B6B'
  calendar.work: '#4ECDC4'
  calendar.family: '#45B7D1'
```

## Configuration options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `title` | string | `'Family Calendar'` | Card title displayed in header |
| `entities` | list | **Required** | List of calendar entity IDs |
| `view_mode` | string | `'month'` | View mode: `'month'`, `'week-compact'`, or `'week-standard'` |
| `default_view` | string | `null` | Initial view mode on load (overrides `view_mode`) |
| `header_color` | string | `'var(--primary-color)'` | Custom header background (solid color or gradient) |
| `first_day_of_week` | integer | `0` | First day of week (`0 = Sunday`, `1 = Monday`, etc.) |
| `week_days` | list | `[0,1,2,3,4,5,6]` | Days to show in week views (`0=Sun`, `6=Sat`) |
| `rolling_days_week_compact` | integer | `null` | Compact week view: show today + N days (alternative to `week_days`) |
| `rolling_days_schedule` | integer | `null` | Schedule view: show today + N days (alternative to `week_days`) |
| `rolling_weeks` | integer | `null` | Show this week + N weeks in month view |
| `week_start_hour` | integer | `8` | Start hour for week-standard view (`0-23`) |
| `week_end_hour` | integer | `21` | End hour for week-standard view (`0-23`) |
| `height_scale` | float | `1.0` | Height scaling factor (`0.5-2.0`, affects schedule view) |
| `compact_height` | boolean | `false` | Fit monthly/schedule views to available screen height without scrolling |
| `compact_header` | boolean | `false` | Single-row header with inline badges |
| `hide_event_calendar_bubble` | boolean | `false` | Hide the calendar initial bubble shown inside events |
| `hide_times_for_calendars` | list | `[]` | Calendar entities whose start/end times should be hidden in schedule view |
| `show_current_time_bar` | boolean | `false` | Show a red current-time indicator line in schedule view |
| `default_dark_mode` | boolean | `false` | Start the card in dark mode on load (legacy alias: `dark_mode`) |
| `show_week_numbers` | boolean | `false` | Show week numbers on the left side |
| `max_events` | integer | `100` | Maximum number of events to load |
| `enable_event_management` | boolean | `true` | Enable event creation features |
| `readonly_calendars` | list | `[]` | Calendar entities that should not allow modifications |
| `colors` | map | auto | Custom colors for each calendar entity |
| `language` | string | `en` | Language for strings |
| `locale` | string | `en-US` | Optional locale; falls back to language/Home Assistant settings |

## Features in detail: appearance and colors

### Color-coded events

Each calendar entity can have its own color:

```yaml
colors:
  calendar.personal: '#FF6B6B'    # Red for personal events
  calendar.work: '#4ECDC4'        # Teal for work events
  calendar.family: '#45B7D1'      # Blue for family events
  calendar.kids: '#FFA07A'        # Orange for kids' activities
```

### Customizing header color

The header defaults to `var(--primary-color)`, or you can set a custom color/gradient.

**Solid colors:**

```yaml
header_color: '#1e40af'
header_color: '#059669'
header_color: '#dc2626'
```

**Gradients:**

```yaml
header_color: 'linear-gradient(135deg, #1e3a8a 0%, #3b82f6 100%)'
header_color: 'linear-gradient(135deg, #065f46 0%, #10b981 100%)'
header_color: 'linear-gradient(135deg, #ea580c 0%, #dc2626 100%)'
header_color: 'linear-gradient(135deg, #0f766e 0%, #14b8a6 100%)'
header_color: 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)'
```

**Theme variables:**

```yaml
header_color: 'var(--secondary-color)'
header_color: 'var(--accent-color)'
header_color: 'var(--card-background-color)'
header_color: 'var(--primary-color)'
```
