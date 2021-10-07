# Finnhub

Display Finnhub stocks for the configured symbols.

## Configuration

```yaml
finnhub:
  apiKey: "your-api-key"
  symbols:
    - "AAPL"
    - "MSFT"
    - "AMZN"
    - "FSLY"
  enabled: true
  position:
    top: 0
    left: 0
    height: 2
    width: 2
  refreshInterval: 5
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="apiKey", desc="Your finnhub.io api key.", value="A valid API key." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="symbols", desc="List of symbols to display.", value="List of symbols." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="stocks/finnhub" %}
{% include "src_path.md" %}