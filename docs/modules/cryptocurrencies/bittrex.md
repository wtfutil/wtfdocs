# Bittrex

Get the last 24 hour summary of cryptocurrencies market using [Bittrex](https://bittrex.com).

## Configuration

```yaml
bittrex:
  colors:
    base:
      name: orange
      displayName: red
    market:
      name: red
      field: white
      value: green
  enabled: true
  position:
    top: -2
    left: 2
    height: 3
    width: 1
  refreshInterval: 5s
  summary:
    BTC:
      displayName: Bitcoin
      market:
      - LTC
      - ETH
```

## Screenshots

<img class="screenshot" src="/assets/modules/bittrex.png" width="320" height="412" alt="bittrex screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>colors.base.dispayName</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.base.name</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.market.field</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.market.name</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.market.value</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
    </tbody>
</table>

{% set src="cryptoexchanges/bittrex" %}
{% include "src_path.md" %}