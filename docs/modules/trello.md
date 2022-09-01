# Trello

Displays all Trello cards on specified lists.

## Configuration

### Single Trello List

```yaml
trello:
  accessToken: "d23*******************************************3r2"
  apiKey: "p0d13*********************************************c3"
  board: Main
  enabled: true
  list: "Todo"
  position:
    height: 1
    left: 2
    top: 0
    width: 1
  refreshInterval: 1h
  username: myname
```

### Multiple Trello Lists

If you want to monitor multiple Trello lists, use the following
configuration (note the difference in `list`):

```yaml
trello:
  accessToken: "d23*******************************************3r2"
  apiKey: "p0d13*********************************************c3"
  board: Main
  enabled: true
  list: ["Todo", "Done"]
  position:
    height: 1
    left: 2
    top: 0
    width: 1
  refreshInterval: 1h
  username: myname
```

## Screenshots

<img class="screenshot" src="/assets/modules/trello.png" width="640" height="197" alt="trello screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="accessToken", desc="Your Trello access token. Leave empty to use the <code>WTF_TRELLO_ACCESS_TOKEN</code> environment variable.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="Trello", envvar="WTF_TRELLO_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="board", desc="The name of the Trello board.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="list", desc="The Trello lists to fetch cards from.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Trello" %}
        {% include "attributes/username.md" %}

    </tbody>
</table>

{% set src="todo_plus" %}
{% include "src_path.md" %}
