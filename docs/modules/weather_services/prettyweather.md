# Pretty Weather

Displays weather information as ASCII art from [Wttr.in](http://wttr.in).

Consider using wego directly, to avoid issues with rate limiting.
See [wego](../../cmdrunner/wego).

## Configuration

```yaml
prettyweather:
    enabled: true
    city: "tehran"
    position:
        top: 3
        left: 5
        height: 1
        width: 1
    refreshInterval: 5m
    unit: "m"
    view: 0
    language: "en"
```

<img class="screenshot" src="/assets/modules/prettyweather.png" width="320" height="191" alt="prettyweather screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="city", desc="<em>Optional</em> The name of the city to display weather for. Default: <code>Barcelona</code>.", value="The name of any city supported by <a href='http://wttr.in'>Wttr.in</a>." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="language", desc="<em>Optional</em> Wttr.in language configuration. Default: <code>en</code>.", value="See <code>curl wttr.in/:translation</code> for more details." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="unit", desc="<em>Optional</em> The scale to display temperatures in. Default: <code>m</code>.", value="<code>u</code> for Fahrenheit, <code>m</code> for Celsius." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="view", desc="<em>Optional</em> Wttr.in view configuration.", value="See <code>curl wttr.in/:help</code> for more details." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>


{% set src="weatherservices/prettyweather" %}
{% include "src_path.md" %}