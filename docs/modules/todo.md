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

        {% with name="checkedPos", desc="<em>Optional</em> The position at which the checkbox is shown. <br />Default: <code>first</code>", value="<code>first</code>, <code>last</code>, <code>none</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
        
        {% with name="dates.enabled", desc="<em>Optional</em> Whether or not the following <code>date</code> functionality is enabled. <br />Default: <code>true</code>", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="dates.format", desc="<em>Optional</em> The format in which to display dates. <br />Default: <code>yyyy-mm-dd</code>", value="<code>yyyy-mm-dd</code>, <code>yy-mm-dd</code>, <code>dd-mm-yy</code>, <code>dd-mm-yyyy</code>, <code>dd M yy</code>, <code>dd M yyyy</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="dates.hideYearIfCurrent", desc="<em>Optional</em> Hide the year, if the todo item year is the current year. <br />Default: <code>true</code>", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="dates.switchToInDays", desc="<em>Optional</em> The number of days in the future after which the todo item date is displayed as an absolute date. <br />Default: <code>7</code>", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="dates.undatedAsDays", desc="<em>Optional</em> How many days into the future undated todo items should be considered 'due'. <br />Default: <code>7</code>", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="filename", desc="The name for the todo file.", value="Any valid filename, ideally ending in <code>yml</code>." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="newPos", desc="<em>Optional</em> The position into which new todo items are created. <br />Default: <code>first</code>", value="<code>first</code>, <code>last</code>" %}
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

    {% set ctrlf="Move the selected item to the top of the list" %}
    {% include "keyboard/ctrlf.md" %}

    {% set ctrlj="Move the selected item down the list" %}
    {% include "keyboard/ctrlJ.md" %}

    {% set ctrlk="Move the selected item up the list" %}
    {% include "keyboard/ctrlK.md" %}

    {% set ctrll="Move the selected item to the bottom of the list" %}
    {% include "keyboard/ctrll.md" %}
  </tbody>
</table>

{% set src="todo" %}
{% include "src_path.md" %}