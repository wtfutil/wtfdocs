# Yahoo Finance

Display Yahoo Finance data for the configured symbols.

The first column shows the symbol's status:

* pre-market: ⏭
* open: ▶
* post-market: ⏮
* closed: ⏹

The second column is the symbol's shortname, third column shows the current value.
The fourth columns will show a different icon depending on the current market change:

* >3%: ⬆️
* >0%: ↗️
* <0%: ↘️
* <-3%: ⬇️

## Configuration

```yaml
yfinance:
  enabled: true
  title: "Stocks 🚀"
  sort: true
  refreshInterval: 60
  symbols:
    - "DOCN"
    - "GLE.PA"
    - "ABN.AS"
    - "ICAD.PA"
    - "ACA.PA"
    - "ORA.PA"
  position:
    top: 1
    left: 0
    height: 1
    width: 1
```

## Screenshots

<img class="screenshot" src="/imgs/modules/yfinance.png" width="414" height="285" alt="yfinance screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="symbols", desc="List of Yahoo Finance symbols to display.", value="List of valid Yahoo Finance symbols." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="sort", desc="<em>Optional</em> Sort indices by market change percent. Default: <code>false</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="yfinance" %}
{% include "src_path.md" %}