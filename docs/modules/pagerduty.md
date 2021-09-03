![pagerduty](/assets/services/pagerduty.png){: align=left width=128 height=128}

# PagerDuty

Shows Pagerduty on-call schedules.

## Configuration

```yaml
pagerduty:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  escalationFilter:
  - "client-eng"
  position:
    top: 4
    left: 3
    height: 1
    width: 2
  scheduleIDs:
  - "R2D24CD"
  - "C3P05MF"
  showIncidents: true
  showOnCallEnd: true
  showSchedules: true
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="PagerDuty", envvar="WTF_PAGERDUTY_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="escalationFilter", desc="An array of schedule names you want to filter on." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="scheduleIDs", desc="An array of schedule IDs you want to restrict the query to." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
        
        {% with name="showIncidents", desc="<em>Optional</em> Whether or not to list incidents. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showOnCallEnd", desc="<em>Optional</em> Whether or not to display the end date of the oncall rotation. Default: <code>false</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showSchedules", desc="<em>Optional</em> Whether or not to show schedules. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="teamIDs", desc="<em>Optional</em> An array of team IDs to restrict the incidents query to.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="userIDs", desc="<em>Optional</em> An array of user IDs to restrict the incidents query to.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="pagerduty" %}
{% include "src_path.md" %}