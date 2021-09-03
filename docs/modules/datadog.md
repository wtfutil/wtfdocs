# Datadog

Connects to the Datadog API and displays alerting modules.

## Configuration

```yaml
datadog:
  apiKey: "<yourapikey>"
  applicationKey: "<yourapplicationkey>"
  enabled: true
  monitors:
    tags:
      - "team:ops"
  position:
    top: 4
    left: 3
    height: 1
    width: 2
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Datadog", envvar="WTF_DATADOG_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}
    </tbody>
<tr>
    <td>
        <code>applicationKey</code>
        <br />
        Your DataDog application key. Leave this empty to use the <code>WTF_DATADOG_APPLICATION_KEY</code> environment variable.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>monitors</code>
        <br />
        Configuration for the monitors functionality.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>tags</code>
        <br />
        List of tags you want to query monitors by.
    </td>
    <td></td>
</tr>
</table>

{% set src="datadog" %}
{% include "src_path.md" %}