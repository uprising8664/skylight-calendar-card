# Skylight Calendar Card for Home Assistant

A custom Lovelace calendar card inspired by the Skylight Calendar style.

## Prerequisite

This card requires one or more **Home Assistant calendar entities** (for example: `calendar.family`, `calendar.work`, etc.).

## Quick Start

### 1) Install

Install with **HACS** (recommended):

1. Open HACS → **Frontend**
2. Search for **Skylight Calendar Card**
3. Download and restart Home Assistant

Or install manually by copying `skylight-calendar-card.js` to `/config/www/` and adding it as a Lovelace resource.

### 2) Add the card

Use this simple, working example:

```yaml
type: custom:skylight-calendar-card
title: Family Calendar
entities:
  - calendar.family
```

## Documentation Wiki

Full documentation has been moved to the wiki pages in this repository:

- [Wiki Home](wiki/Home.md)
- [Installation](wiki/Installation.md)
- [Configuration](wiki/Configuration.md)
- [Views & Navigation](wiki/Views-and-Navigation.md)
- [Event Management](wiki/Event-Management.md)
- [Troubleshooting](wiki/Troubleshooting.md)
- [Compatibility with Card Mod](wiki/Compatibility-with-Card-Mod.md)
- [Development](wiki/Development.md)

You can also browse by topic via the wiki sidebar: [Wiki Sidebar](wiki/_Sidebar.md).
