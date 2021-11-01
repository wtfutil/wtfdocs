# Textfile

Displays the contents of the specified text file in the widget.

## Configuration

```yaml
textfile:
  enabled: true
  filePaths:
  - "~/Desktop/notes.md"
  - "~/.config/wtf/config.yml"
  format: true
  formatStyle: "dracula"
  position:
    top: 5
    left: 4
    height: 2
    width: 1
  refreshInterval: 15s
  wrapText: true
```

## Screenshots

<img class="screenshot" src="/assets/modules/textfile.png" width="320" height="133" alt="textfile screenshot" />

## Attributes

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
{% with name="filePaths", desc="An array of paths to the files to be displayed in the widget.", value="" %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="format", desc="<em>Optional</em> Whether or not to try and format and syntax highlight the displayedtext. Default: <code>false</code>", value="<code>true</code>, <code>false</code>" %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="formatStyle", desc="<em>Optional</em> The style of syntax highlighting to format the text with. Default: <code>vim</code>", value="See <a href='https://github.com/alecthomas/chroma/tree/master/styles'>Chroma styles</a> for all valid options." %}
{% include "attributes/custom.md" %}
{% endwith %}

{% include "attributes/wrapText.md" %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}
    {% set return="Opens the text file in whichever text editor is associated  with that file type" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Select the previous file" %}
    {% include "keyboard/h.md" %}

    {% set l="Select the next file" %}
    {% include "keyboard/l.md" %}

    {% set o="Opens the text file in whichever text editor is associated  with that file type" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Select the previous file" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Select the next file" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="textfile" %}
{% include "src_path.md" %}