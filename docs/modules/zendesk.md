# Zendesk

Displays Zendesk tickets.

## Configuration

```yaml
zendesk:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 0
    left: 2
    height: 1
    width: 1
  status: "new"
  subdomain: "your_domain"
  username: "your_email@acme.com"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Zendesk", envvar="ZENDESK_API" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="status", desc="The status of tickets you want to retrieve.", value="<code>new</code>, <code>open</code>, <code>pending</code>, <code>hold</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="subdomain", desc="Your Zendesk subdomain. Leave this empty to use the <code>ZENDESK_SUBDOMAIN</code> environment variable.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

    {% set name="Zendesk" %}
    {% include "attributes/username.md"  %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected ticket in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="zendesk" %}
{% include "src_path.md" %}