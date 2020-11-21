# NBA Score

Displays NBA game scores.

## Configuration

```yaml
nbascore:
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 600
```

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}
   
    {% include "keyboard/spacer.md" %}

    {% set c="Go to current day" %}
    {% include "keyboard/c.md" %}

    {% set h="Go to previous day" %}
    {% include "keyboard/h.md" %}

    {% set l="Go to next day" %}
    {% include "keyboard/l.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Go to previous day" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Go to next day" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="nbascore" %}
{% include "src_path.md" %}