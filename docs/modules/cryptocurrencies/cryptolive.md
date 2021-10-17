# CryptoLive

Compare crypto currencies using [CryptoCompare](https://cryptocompare.com).

## Configuration

```yaml
cryptolive:
  enabled: true
  position:
    top: 5
    left: 2
    height: 1
    width: 2
  updateInterval: 15
  currencies:
    BTC:
      displayName: Bitcoin
      to:
        - USD
        - EUR
        - ETH
        - LTC
        - DOGE
    LTC:
      displayName: Ethereum
      to:
        - USD
        - EUR
        - BTC
  top:
    BTC:
      displayName: Bitcoin
      limit: 5
      to:
        - USD
  colors:
    from:
      name: coral
      displayName: grey
    to:
      name: white
      price: green
    top:
      from:
        name: grey
        displayName: coral
      to:
        name: red
        field: white
        value: green
```

## Screenshots

<img class="screenshot" src="/assets/modules/cryptolive.png" width="320" height="203" alt="cryptolive screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>colors.from.displayName</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.from.name</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.to.name</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>colors.to.price</code>
        <br />
    </td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
</tr>
<tr>
    <td>
        <code>currencies</code>
        <br />
    </td>
    <td></td>
</tr>
    </tbody>
</table>

{% set src="cryptoexchanges/cryptolive" %}
{% include "src_path.md" %}