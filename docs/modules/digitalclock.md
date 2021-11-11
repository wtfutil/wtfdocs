# Digital Clock

Displays a configurable digital clock.

## Configuration

```yaml
digitalclock:
  color: orange
  enabled: true
  font: bigfont
  hourFormat: 12
  position:
    top: 0
    left: 1
    height: 1
    width: 1
  refreshInterval: 1s
  title: "big clock"
  type: "digitalclock"
```

## Screenshots

<img src="/assets/modules/digitalclock.png" class="screenshot" width="240" height="121" alt="digitalclock screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>color</code>
        <br />
        The color to display the clock time in.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>font</code>
        <br />
      The font to display the clock time in. Default: <code>bigfont</code>
    </td>
  <td><code>bigfont</code>, <code>digitalfont</code></td>
</tr>
<tr>
    <td>
        <code>hourFormat</code>
        <br />
        <em>Optional</em> The format of the clock. Default: <code>24</code>.
    </td>
    <td><code>12</code>, <code>24</code></td>
</tr>
    </tbody>
</table>

{% set src="digitalclock" %}
{% include "src_path.md" %}
