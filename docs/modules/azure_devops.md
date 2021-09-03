# Azure Devops

## Configuration

```yaml
azuredevops:
  apiToken: "p0d13*********************************************c3"
  enabled: true
  labelColor: "lightblue"
  maxRows: 3
  orgURL: "https://dev.azure.com/myawesomecompany/"
  position:
    top: 0
    left: 0
    height: 3
    width: 3
  projectName: "the awesome project"
  refreshInterval: 300
  type: "azuredevops"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Azure DevOps", envvar="WTF_AZURE_DEVOPS_API_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        <tr>
            <td>
                <code>labelColor</code>
                <br />
                <em>Optional</em> The color of the title label. Default: <code>white</code>.
                </div>
            </td>
            <td>Any X11 color name.</td>
        </tr>
        <tr>
            <td>
                <code>maxRows</code>
                <br />
                <em>Optional</em> The maximum number of rows to display. Default: <code>3</code>.
            </td>
            <td>Any positive integer.</td>
        </tr>
        <tr>
            <td>
                <code>orgURL</code>
                <br />
                The URL to your Azure DevOps project.
            </td>
            <td>Leave empty to use the <code>WTF_AZURE_DEVOPS_ORG_URL</code> environment variable.</td>
        </tr>
        <tr>
            <td>
                <code>projectName</code>
                <br />
                The name of your Azure DevOps project.
            </td>
            <td>Leave empty to use the <code>WTF_AZURE_DEVOPS_PROJECT_NAME</code> environment variable.</td>
        </tr>
    </tbody>
</table>

{% set src="azuredevops" %}
{% include "src_path.md" %}