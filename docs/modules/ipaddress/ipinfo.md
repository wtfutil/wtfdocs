# IP Info

Displays your current IP address information, from ipinfo.io.

**Note:** IPInfo.io has a free-plan rate limit of 1000 requests per day.

## Configuration

```yaml
ipinfo:
  colors:
    name: red
    value: white
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 150
```

## Screenhots

<img class="screenshot" src="/assets/modules/ipinfo.png" width="320" height="199" alt="ipinfo screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="colors.name", desc="<em>Optional</em> The default colour for the row names." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% with name="colors.value", desc="<em>Optional</em> The default colour for the row values." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="ipinfo" %}
{% include "src_path.md" %}