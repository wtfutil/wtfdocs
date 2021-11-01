# VictorOps

Connects to the VictorOps API and determines who is on call.

## Configuration

```yaml
victorops:
  apiID: a3c5dd63
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 1h
  team: devops
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="apiID", desc="Your <a href='https://help.victorops.com/knowledge-base/api/'>VictorOps API ID</a> token. Leave this empty to use the <code>WTF_VICTOROPS_API_ID</code> environment variable.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="VictorOps", envvar="WTF_VICTOROPS_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="team", desc="<em>Optional</em> Whether or not to only show a specific team. Default: all teams are shown.", value="The team slug that can be found in the URL after <code>/#/team/</code>." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="victorops" %}
{% include "src_path.md" %}