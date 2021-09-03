# Spotify

Control the Spotify client.

## Configuration

```yaml
spotify:
  enabled: true
  colors:
    label: "green"
    text: "white"
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 0
``` 

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="colors.label", desc="<em>Optional</em> The color for labels. Default: <code>green</code>." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% with name="colors.text", desc="<em>Optional</em> The color for text. Default: <code>white</code>." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}
    
    {% set return="Open the selected item in the browser" %}
    {% include "keyboard/return.md" %}

    {% set space="Play/pause the currently-selected song" %}
    {% include "keyboard/space.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Play previous song" %}
    {% include "keyboard/h.md" %}

    {% set l="Play next song" %}
    {% include "keyboard/l.md" %}

    {% include "keyboard/r.md" %}
  </tbody>
</table>

{% set src="spotify" %}
{% include "src_path.md" %}