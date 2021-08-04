# Updown

Connect to the [Updown](https://updown.io) API.

## Configuration

```yaml
updown:
  type: updown
  apiKey: "XXXX"
  tokens:
    - YYYY
  position:
    top: 0
    left: 1
    height: 2
    width: 1
```

## Screenshots

<img class="screenshot" src="/assets/modules/updown.png" width="500" height="316" alt="Updown screenshot" />


## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Updown", envvar="WTF_UPDOWN_APIKEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="apiKey", desc="Updown read-only API-key", value="string" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="tokens", desc="Only show checks with specified tokens", value="list" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="updown" %}
{% include "src_path.md" %}