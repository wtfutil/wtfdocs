# Feed Reader

An RSS & Atom feed reader.

## Configuration

```yaml
feedreader:
  enabled: true
  feeds:
  - https://news.ycombinator.com/rss
  - https://rss.cbc.ca/lineup/topstories.xml
  feedLimit: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 14400
```

## Screenshots

<img class="screenshot" src="/assets/modules/feedreader.png" width="320" height="94" alt="feedreader screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>feedLimit</code>
        <br />
        The number of stories from each feed to be displayed. Default is <code>-1</code>, which will display all available stories.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>feeds</code>
        <br />
        List of RSS or Atom feed URLs.
    </td>
    <td></td>
</tr>
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected story in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}
    
    {% set o="Open the selected story in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% set t="Switches the display mode between `title`, `link`, and `title and content`" %}
    {% include "keyboard/t.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}

  </tbody>
</table>


{% set src="feedreader" %}
{% include "src_path.md" %}