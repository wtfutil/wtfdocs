# Exchange Rates

Displays exchange rates between various currencies.

## Configuration

```yaml
exchangerates:
  enabled: true
  focusable: false
  position:
    top: 4
    left: 4
    width: 1
    height: 2
  precision: 3
  rates:
    CAD:
      - "USD"
      - "EUR"
    USD:
      - "CAD"
    EUR:
      - "CAD"
  title: "💰 Rates"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="precision", desc="<em>Optional</em> The number of decimal places to display. Default: <code>7</code>.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="rates", desc="A key/value list of currencies to convert between.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="exchangerates" %}
{% include "src_path.md" %}