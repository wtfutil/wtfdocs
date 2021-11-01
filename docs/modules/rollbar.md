# Rollbar

Displays item information for your rollbar account.

## Configuration

```yaml
rollbar:
  accessToken: "d23*******************************************3r2"
  enabled: true
  projectOwner: "ENCOM"
  projectName: "MCP"
  activeOnly: true
  assignedToName: "dillinger"
  count: 3
  position:
    top: 4
    left: 1
    height: 2
    width: 2
  refreshInterval: 15m
```

## Screenshots

<img class="screenshot" src="/assets/modules/rollbar.png" width="640" height="187" alt="rollbar screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="accessToken", desc="Your Rollbar project access token (only needs read capabilities).", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="activeOnly", desc="<em>Optional</em> Only show items that are active.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="assignedToName", desc="<em>Optional</em> Set this to your username if you only want to see items assigned to you.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="count", desc="<em>Optional</em> How many items you want to see. 100 is max.", value="Any positive integer up to 100 inclusive." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="projectName", desc="This is used to create a link to the item.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="projectOwner", desc="This is used to create a link to the item.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}
 
    {% set return="Display the selected item in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}
    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="rollbar" %}
{% include "src_path.md" %}