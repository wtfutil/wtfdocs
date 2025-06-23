# UptimeRobot

Learn more about [Uptime Kuma](https://github.com/louislam/uptime-kuma).

As Uptime Kuma does not yet have a full API the module uses data from a single "status page". As such you will need a status page setup with a group of monitored sites, which
is where you get the URL to specify in the configuration.

It's recommended to give this module 2 rows of space in the dashboard, as a second line may appear to display any incident.

<i>This module is based on the similar widget for [Homepage](https://gethomepage.dev/widgets/services/uptime-kuma/).</i>

## Configuration

```yaml
uptimekuma:
  enabled: true
  url: https://uptimekuma.example.com/status/overview
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 1m
```

## Screenshots

<img class="screenshot" src="/assets/modules/uptimekuma.png" width="275" height="320" alt="uptimekuma screenshot" />


## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="url", desc="Full URL of the status page." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="uptimekuma" %}
{% include "src_path.md" %}