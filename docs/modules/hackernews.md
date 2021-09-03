# HackerNews

Displays stories from Hacker News.

## Configuration

```yaml
hackernews:
  enabled: true
  numberOfStories: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  storyType: top
  refreshInterval: 900
```

## Screenshots

<img class="screenshot" src="/assets/modules/hackernews.png" width="320" height="76" alt="hackernews screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="numberOfStories", desc="<code>Optional</code> Defines number of stories to be displayed. Default: <code>10</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="storyType", desc="<code>Optional</code> Defines type of stories to be displayed. Default: <code>top</code>.", value="<code>new</code>, <code>top</code>, <code>job</code>, <code>ask</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected story in the browser" %}

    {% include "keyboard/spacer.md" %}

    {% set c="Open the selected story's comments in the browser" %}
    {% include "keyboard/c.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set o="Open the selected story in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="hackernews" %}
{% include "src_path.md" %}