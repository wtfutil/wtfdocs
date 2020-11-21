# Google Spreadsheet

Display information from cells in a Google Spreadsheet.

## Configuration

```yaml
gspreadsheets:
  colors:
    values: "green"
  cells:
    names:
    - "Cell 1 name"
    - "Cell 2 name"
    addresses:
    - "A1"
    - "A2"
  enabled: true
  position:
    top: 0
    left: 0
    width: 1
    height: 1
  refreshInterval: "300"
  secretFile: "~/.config/wtf/gspreadsheets/client_secret.json"
  sheetId: "id_of_google_spreadsheet"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="colors.values", desc="<em>Optional</em> The color to display the cell values in." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% with name="colors.names", desc="<em>Optional</em>" %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% with name="colors.addresses", desc="<em>Optional</em>" %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% with name="secretFile", desc="Your <a href='https://developers.google.com/calendar/quickstart/go'>Google client secret</a> JSON file.", value="A string representing a file path to the JSON secret file." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="gspreadsheets" %}
{% include "src_path.md" %}