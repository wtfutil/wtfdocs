# OpsGenie

Shows OpsGenie on-call schedules.

See <a href="https://docs.opsgenie.com/docs/who-is-on-call-api">Who is on Call API</a> for details. 

## Configuration

### Single Schedule

```yaml
opsgenie:
  apiKey: "p0d13*********************************************c3"
  displayEmpty: false
  enabled: true
  position:
    top: 2
    left: 1
    height: 2
    width: 1
  refreshInterval: 6h
  region: "us"
  schedule: "Primary"
  scheduleIdentifierType: "id"
```

### Multiple Schedules

```yaml
opsgenie:
  apiKey: "p0d13*********************************************c3"
  displayEmpty: false
  enabled: true
  position:
    top: 2
    left: 1
    height: 2
    width: 1
  refreshInterval: 6h
  region: "us"
  schedule:
  - "Primary"
  - "Secondary"
  scheduleIdentifierType: "id"
```

## Screenshots

<img class="screenshot" src="/assets/modules/opsgenie.png" width="320" height="389" alt="opsgenie screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="OpsGenie", envvar="WTF_OPS_GENIE_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="displayEmpty", desc="Whether schedules with no assigned person on-call should be displayed. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="region", desc="The region of the servers to connect to.", value="<code>eu</code>, <code>us</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="scheduleIdentifierType", desc="Type of the schedule identifier.", value="<code>id</code>, <code>name</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

    </tbody>
</table>

{% set src="opsgenie" %}
{% include "src_path.md" %}