# Todo

An interactive todo list.

## Configuration

```yaml
todo:
  checkedIcon: "X"
  colors:
    checked: gray
    highlight:
      fore: "black"
      back: "orange"
  enabled: true
  filename: "todo.yml"
  position:
    top: 2
    left: 2
    height: 2
    width: 1
  refreshInterval: 3600
```

## Screenshots

<img class="screenshot" src="/assets/modules/todo.png" width="320" height="388" alt="todo screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="checked", desc="The foreground color for checked rows.", value="" %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% include "attributes/colors/highlight.md" %}

        {% with name="checkedIcon", desc="<em>Optional</em> The icon used to denote a 'checked' todo item.", value="Any displayable unicode character." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="filename", desc="The name for the todo file.", value="Any valid filename, ideally ending in <code>yml</code>." %}
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

    {% set esc="Close the modal item dialog without saving changes" %}
    {% include "keyboard/esc.md" %} 

    {% set return="Edit the selected item" %}
    {% include "keyboard/return.md" %} 

    {% set return="Close the modal item dialog and save changes" %}
    {% include "keyboard/return.md" %} 

    {% set space="Check/uncheck the selected item" %}
    {% include "keyboard/space.md" %} 

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set n="Create a new list item" %}
    {% include "keyboard/n.md" %}

    {% set o="Opens the todo list file in whichever text editor is associated with that file type" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/ctrlD.md" %}

    {% set ctrlj="Move the selected item down the list" %}
    {% include "keyboard/ctrlJ.md" %}

    {% set ctrlk="Move the selected item up the list" %}
    {% include "keyboard/ctrlK.md" %}
  </tbody>
</table>

{% set src="todo" %}
{% include "src_path.md" %}