# Krisinformation

Displays important messages from Krisinformation.se which is a web site run by
the Swedish Civil Contingencies Agency that compiles and convey warnings,
alerts, and emergency information from Swedish authorities to the public.

 - [Krisinformation](https://www.krisinformation.se/en/).

## Configuration

```yaml
krisinformation:
  title: Krisinformation
  enabled: true
  latitude: 53.1234
  longitude: 12.1234
  radius: -1
  country: true
  maxitems: 5
  maxage: 1000
  refreshInterval: 3600
  position:
    top: 0
    left: 0
    height: 1
    width: 3
```

## Screenshots

<img class="screenshot" src="/assets/modules/krisinformation.png" width="688" height="420" alt="Krisinformation screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="latitude", desc="<em>Optional</em> The latitude of the position from which the widget should look for messages.", value="Decimal degrees" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

         {% with name="longitude", desc="<em>Optional</em> The longitude of the position from which the widget should look for messages.", value="Decimal degrees" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="radius", desc="<em>Optional</em> The radius in km from your position that the widget should look for messages, use latitude/longitude setting", value="Any positive integer" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="county", desc="<em>Optional</em> The county from where to display messages", value="string" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="country", desc="<em>Optional</em> Only display country wide messages. Default: <code>true</true>", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="maxitems", desc="<em>Optional</em> Only display X number of latest messages. (-1 disables) Default: <code>-1</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="maxage", desc="<em>Optional</em> Only show messages younger than maxage in hours. Default: <code>720</code>", value="Any positive integer" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="krisinformation" %}
{% include "src_path.md" %}
