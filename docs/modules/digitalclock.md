# Digital Clock

Displays a configurable digital clock.

## Configuration

<img src="/assets/modules/digitalclock.png" class="screenshot" width="240" height="121" alt="digitalclock screenshot" />

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

## Configuration - compact variant

Set `withDatePrefix` to `False` and pass in a custom `dateFormat` according to go.

<img src="/assets/modules/digitalclock-small.png" class="screenshot" width="240" height="121" alt="digitalclock screenshot" />

```yaml
digitalclock:
  withDatePrefix: False
  dateFormat: "Monday Jan 02 2006"
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
<tr>
    <td>
        <code>dateFormat</code>
        <br />
        <em>Optional</em> The format of the date. Default: <code>Monday January 02 2006</code>.
    </td>
    <td>Any valid Go date layout which is handled by <a href="https://golang.org/src/time/format.go">Time.Format.</a>
    </td>
</tr>
<tr>
    <td>
        <code>withDatePrefix</code>
        <br />
        <em>Optional</em> Whether to display `Date:` in front of the date. Default: <code>True</code>.
    </td>
    <td><code>True</code>, <code>False</code></td>
</tr>
    </tbody>
</table>

{% set src="digitalclock" %}
{% include "src_path.md" %}
