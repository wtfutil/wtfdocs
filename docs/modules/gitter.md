# Gitter

Displays chat messages from Gitter.

## Configuration

```yaml
gitter:
  apiToken: "d23*******************************************3r2"
  enabled: true
  numberOfMessages: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 4
  roomUri: wtfutil/Lobby
  refreshInterval: 5m
```

## Screenshots

<img src="/assets/modules/gitter.png" width="847" height="160" alt="gitter screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Gitter", envvar="WTF_GITTER_API_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="numberOfMessages", desc="<code>Optional</code> Maximum number of <em>new</em> messages to be displayed. Default is <code>10</code>.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="roomURI", desc="<code>Optional</code> URI of the room you would like to see the chat messages for. Default is <code>wtfutil/Lobby</code>", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}
    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
</table>

{% set src="gitter" %}
{% include "src_path.md" %}