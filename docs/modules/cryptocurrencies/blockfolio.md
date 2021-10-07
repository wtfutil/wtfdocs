# Blockfolio

Display your Blockfolio crypto holdings.

## Configuration

```yaml
blockfolio:
  colors:
    name: blue
    grows: green
    drop: red
  device_token: "device token"
  displayHoldings: true
  enabled: true
  position:
    top: 3
    left: 1
    width: 1
    height: 1
  refreshInterval: 400
```

## Screenshots

<img class="screenshot" src="/assets/modules/blockfolio.png" width="320" height="185" alt="blockfolio screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        <tr>
            <td>
                <code>colors.drop</code>
                <br />
            </td>
            <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
        </tr>
        <tr>
            <td>
                <code>colors.grows</code>
                <br />
            </td>
            <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
        </tr>
        <tr>
            <td>
                <code>colors.name</code>
                <br />
            </td>
            <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color name</a> or long-form hex value (i.e.:
        <code>#ff0000</code>).</td>
        </tr>
        <tr>
            <td>
                <code>device_token</code>
                <br />
                See <a href="https://github.com/bob6664569/blockfolio-api-client">this gist</a> for details on how to get your Blockfolio API token.
            </td>
            <td></td>
        </tr>
    </tbody>
</table>

{% set src="cryptoexchanges/blockfolio" %}
{% include "src_path.md" %}
