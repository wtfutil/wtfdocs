# New Relic

Connects to the New Relic API and displays the last n deploys of the
monitored applications: deploy ID, deploy time, and who deployed it.

## Configuration

```yaml
newrelic:
  apiKey: "p0d13*********************************************c3"
  applicationIDs:
    - 10549735
    - 499785
  deployCount: 6
  enabled: true
  position:
    top: 4
    left: 3
    height: 1
    width: 2
  refreshInterval: 15m
```

## Screenshots

<img class="screenshot" src="/assets/modules/newrelic.png" width="640" height="189" alt="newrelic screenshot" class="clearfix" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="New Relic", envvar="WTF_NEW_RELIC_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="applicationIds", desc="A list of integer IDs of the New Relic applications you wish to report on.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="deployCount", desc="<em>Optional</em> The number of past deploys to display on screen. Default: <code>5</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous application" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next application" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="newrelic" %}
{% include "src_path.md" %}