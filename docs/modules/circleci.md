# CircleCI

Displays build information for your CircleCI account.

## Configuration

```yaml
circleci:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  numberOfBuilds: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 15m
```

## Screenshots

<img src="/assets/modules/circleci.png" class="screenshot" width="609" height="150" alt="circleci screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="CircleCI", envvar="WTF_CIRCLE_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="numberOfBuilds", desc="How many builds to display", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="circleci" %}
{% include "src_path.md" %}
