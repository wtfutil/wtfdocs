# UptimeRobot

Connect to the [UptimeRobot](https://uptimerobot.com) API.

## Configuration

```yaml
uptimerobot:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  offlineFirst: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 1h
  uptimePeriods: 7-30
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="UptimeRobot", envvar="WTF_UPTIMEROBOT_APIKEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="offlineFirst", desc="<em>Optional</em> Display offline monitors at the top.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="uptimePeriods", desc="<em>Optional</em> he periods over which to display uptime (in days, dash-separated).", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="uptimerobot" %}
{% include "src_path.md" %}