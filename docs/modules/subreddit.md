# Subreddit

Displays stories from a specific subreddit.

## Configuration

```yaml
subreddit:
  enabled: true
  numberOfPosts: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 15m
  sortOrder: top
  subreddit: "news"
  topTimePeriod: month
```

## Screenshots

<img class="screenshot" src="/assets/modules/subreddit.png" width="320" height="76" alt="subreddit module screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="numberOfPosts", desc="<em>Optional</em> Defines number of stories to be displayed. Default: <code>10</code>. Note that the module only makes one request, so the maximum is 25.", value="Any positive integer equal to or less than 25." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="sortOrder", desc="<em>Optional</em> Defines the order to sort the posts in the subreddit. Default: <code>hot</code>.", value="<code>new</code>, <code>top</code>, <code>hot</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="subreddit", desc="The subreddit to display links from.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="topTimePeriod", desc="<em>Optional</em> Defines the time period to choose top posts from. Default: <code>all</code>.", value="<code>hour</code>, <code>day</code>, <code>week</code>, <code>month</code>, <code>year</code>, <code>all</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected link in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set c="Open the selected link's Reddit comments in the browser" %}
    {% include "keyboard/c.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set o="Open the selected link in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="subreddit" %}
{% include "src_path.md" %}
