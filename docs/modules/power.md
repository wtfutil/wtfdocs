# Power

Displays information about the current power source.

For battery, also displays the current charge, estimated time remaining, and whether it is charging or discharging.

## Configuration

```yaml
power:
  enabled: true
  position:
    top: 5
    left: 0
    height: 2
    width: 1
  refreshInterval: 15
```

## Screenshots

<img class="screenshot" src="/assets/modules/power.png" width="320" height="129" alt="power screenshot" />

{% set src="power" %}
{% include "src_path.md" %}