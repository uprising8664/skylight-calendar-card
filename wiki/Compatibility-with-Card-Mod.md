# Compatibility with Card Mod

`skylight-calendar-card` does **not** officially support Card Mod.

That said, some users have reported success adjusting certain visual parameters by wrapping this card with `custom:mod-card` and applying targeted CSS.

## Example: adjust calendar badge padding

```yaml
type: custom:mod-card
card:
  type: custom:skylight-calendar-card
  title: Family Calendar
  entities:
    - calendar.test
card_mod:
  debug: true
  style:
    skylight-calendar-card $: |
      .calendar-container .calendar-badges {
        padding-top: 8px;
        padding-bottom: 8px;
      }
```

## Example: increase overall font size

```yaml
card_mod:
  debug: true
  style:
    skylight-calendar-card $: |
      :host * {
        font-size: 22px !important;
      }
```

## Notes

- Because this is unofficial, behavior may vary by Home Assistant/Card Mod version.
- CSS selectors may break if the card internals change in future releases.
- If something stops working after an update, re-check selectors using Card Mod debug tools.
