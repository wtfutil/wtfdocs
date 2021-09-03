---
title: "Google Spreadsheets"
date: 2018-06-10T18:26:26-04:00
draft: false
weight: 50
---

Display information from cells in a Google Spreadsheet.

## Configuration

{{< code lang="yaml" >}}
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
{{< /code >}}

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="colors.values" desc="The color to display the cell values in." >}}
  {{< attributes/custom name="cells.names" desc="" >}}
  {{< attributes/custom name="cells.addresses" desc="" >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

  <tr>
    <td>`secretFile`</td>
    <td>Your <a href="https://developers.google.com/sheets/api/quickstart/go">Google client secret</a> JSON file.</td>
    <td>A string representing a file path to the JSON secret file.</td>
  </tr>
{{% /attributes %}}

{{% sourcePath module="gspreadsheets" %}}