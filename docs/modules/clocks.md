# Clocks

Displays a configurable list of world clocks, the local time, and date.

## Configuration

```yaml
clocks:
  colors:
    rows:
      even: "lightblue"
      odd: "white"
  enabled: true
  locations:
    # From https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
    - Avignon: "Europe/Paris"
    - Barcelona: "Europe/Madrid"
    - Dubai: "Asia/Dubai"
    - New York: "America/New York"
    - Toronto: "America/Toronto"
    - UTC: "Etc/UTC"
    - Vancouver: "America/Vancouver"
  position:
    top: 4
    left: 0
    height: 1
    width: 1
  refreshInterval: 15
  # Valid options are: alphabetical, chronological, natural
  sort: "alphabetical"
```

## Screenshots

<img src="/assets/modules/clocks.png" class="screenshot" width="320" height="191" alt="clocks screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        <tr>
            <td>
                <code>dateFormat</code>
                <br />
                The format of the date strings.
            </td>
            <td>Any valid Go date layout which is hadled by <a href="https://golang.org/src/time/format.go">Time.Format.</a>
            </td>
        </tr>
        <tr>
            <td>
                <code>timeFormat</code>
                <br />
                The fomat of the time strings.
            </td>
            <td>Any valid Go time layout which is handled by <a href="https://golang.org/src/time/format.go">Time.Format.</a>
            </td>
        </tr>
        <tr>
            <td>
                <code>locations</code>
                <br />
                A list of timezone for the clocks to be displayed.
            </td>
            <td>Any <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">TZ database timezone.
            </td>
        </tr>
        <tr>
            <td>
                <code>sort</code>
                <br />
                The order in which to sort the clocks.
            </td>
            <td>
                <code>alphabetical</code>, <code>chronological</code>, or <code>natural</code>. 
                <br />
                <br />
                <code>alphabetical</code> will sort in acending order by <code>key</code>.
                <br />
                <code>chronological</code> will sort in ascending order by date/time.
                <br />
                <code>natural</code> will maintain the config file ordering.
            </td>
        </tr>
    </tbody>
</table>

{% set src="clocks" %}
{% include "src_path.md" %}