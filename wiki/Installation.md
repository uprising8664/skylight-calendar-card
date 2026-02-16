# Installation

## HACS (Recommended)

1. Make sure [HACS](https://hacs.xyz/) is installed
2. In HACS, open **Frontend**
3. Click **+ Explore & Download Repositories**
4. Search for **Skylight Calendar Card**
5. Download and restart Home Assistant

## Manual installation

1. Download `skylight-calendar-card.js` from the latest release
2. Copy it to `<config>/www/skylight-calendar-card.js`
3. Add this to Lovelace resources:

```yaml
resources:
  - url: /local/skylight-calendar-card.js
    type: module
```

4. Restart Home Assistant
