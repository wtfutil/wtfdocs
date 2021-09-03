# IP-API

Displays your current IP address information, from [IP-API.com](http://ip-api.com).

**Note:** IP-API.com has a free-plan rate limit of 120 requests per
minute.

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

{% set src="ipapi" %}
{% include "src_path.md" %}