# Pocket

Displays Pocket Saved Articles.

## Configuration

```yaml
pocket:
    enabled: true
    position:
        top: 0
        left: 3
        height: 4
        width: 2
    consumerKey: '88*******************'
    refreshInterval: 1
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="consumer_key", desc="The consumer key of Pocket app obtained from <a href='https://getpocket.com/developer/apps/new'>https://getpocket.com/developer/apps/new</a>. Make sure to have <code>add</code>, <code>modify</code>, and <code>retrieve</code> permissions.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the article in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set a="Toggle link archive/unarchive" %}
    {% include "keyboard/a.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set t="Toggle view archived links/active links" %}
    {% include "keyboard/t.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="pocket" %}
{% include "src_path.md" %}