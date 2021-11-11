# COVID

Provides details about COVID-19 cases and deaths.

## Configuration

```yaml
covid:
  enabled: true
  colors:
    label: "green"
    text: "white"
  countries:
    - AD
    - AE
    - AF
  position:
    top: 1
    left: 2
    height: 2
    width: 2
  refreshInterval: 1h
``` 

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>countries</code>
        <br />
        The list of country codes (ISO 3166-1 alpha-2) to display detailed information for.
    </td>
    <td></td>
</tr>
    </tbody>
</table>

## Screenshots

<img src="/assets/modules/covid.png" class="screenshot" width="300" height="600" alt="covid screenshot" />

{% set src="covid" %}
{% include "src_path.md" %}