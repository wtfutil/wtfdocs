# Todoist

Displays all items on specified project.

## Configuration

```yaml
todoist:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 0
    left: 2
    height: 1
    width: 1
  projects:
    - 122247497
  refreshInterval: 1h
```

## Screenshots

<img class="screenshot" src="/assets/modules/todoist.png" alt="todoist screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Todoist", envvar="WTF_TODOIST_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="projects", desc="The todoist projects to fetch items from.", value="The integer ID of the project." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set esc="Remove focus from the selected item" %}
    {% include "keyboard/esc.md" %}

    {% include "keyboard/spacer.md" %}

    {% set c="Close current item" %}
    {% include "keyboard/c.md" %}

    {% set d="Delete current item" %}
    {% include "keyboard/d.md" %}

    {% set h="Show the previous project" %}
    {% include "keyboard/h.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set l="Show the next project" %}
    {% include "keyboard/l.md" %}

    {% set u="Clear the current selection" %}
    {% include "keyboard/u.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous project" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next project" %}
    {% include "keyboard/arrowFore.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="todo_plus" %}
{% include "src_path.md" %}
