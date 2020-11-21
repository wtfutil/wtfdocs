# BambooHR

## Configuration

```yaml
bamboohr:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 900
  subdomain: "testco"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="BambooHR", envvar="WTF_BAMBOO_HR_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        <tr>
            <td>
                <code>subdomain</code>
                <br />
                Your <a href="https://www.bamboohr.com/api/documentation/">BambooHR API</a> subdomain name. Leave this blank to use the <code>WTF_BAMBOO_HR_SUBDOMAIN</code> environment variable.
            </td>
            <td></td>
        </tr>
    </tbody>
</table>

{% set src="bamboohr" %}
{% include "src_path.md" %}