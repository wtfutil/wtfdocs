# FXMacroData

Displays the next scheduled macroeconomic releases (CPI prints, rate decisions, payrolls and so on) for the configured currencies, soonest first, using the [FXMacroData](https://fxmacrodata.com/?utm_source=github&utm_medium=referral&utm_campaign=wtfdocs) release calendar.

Each line shows the release time in your local timezone, the currency and the release name. Releases marked top tier for their currency are shown in bold. A `~` in the first column means the date is still provisional rather than confirmed by the publishing authority.

USD data is public, so the module works without an API key. A key is needed for the other currencies. If a currency in the list is not covered by your key it is skipped and the rest are still shown.

## Configuration

```yaml
fxmacrodata:
  enabled: true
  currencies:
    - "USD"
    - "EUR"
  count: 10
  topTier: true
  refreshInterval: 15m
  position:
    top: 0
    left: 0
    height: 2
    width: 2
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="FXMacroData", envvar="FXMACRODATA_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="currencies", desc="<i>Optional</i> The currency codes to show releases for. Default: <code>USD</code>.", value="A list of currency codes, for example <code>USD</code>, <code>EUR</code>, <code>GBP</code>." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="count", desc="<i>Optional</i> The number of upcoming releases to display. Default: <code>10</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="topTier", desc="<i>Optional</i> Only show releases marked top tier for their currency. Default: <code>false</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% include "attributes/enabled.md" %}
        {% include "attributes/position.md" %}

        <tr>
            <td>
                <code>refreshInterval</code>
                <br />
                <i>Optional</i> How often this module will update its data. Default: <code>15m</code>.
            </td>
            <td>Any valid time duration.</td>
        </tr>

        {% include "attributes/title.md" %}
    </tbody>
</table>

{% set src="fxmacrodata" %}
{% include "src_path.md" %}
