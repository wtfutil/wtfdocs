# Azure Logs

Displays results from an Azure - Log Analytics Workspace query.

## Configuration

```yaml
azurelogs:
  title: web request stats
  enabled: true
  queryFile: "queries/web_stats.yaml"
  position:
    top: 2
    left: 0
    height: 1
    width: 1
  refreshInterval: 30
```

example query file `queries/web_stats.yaml`:

```yaml
azure_subscription_id: 6a258992-8b46-4657-ae2f-1384f2c94af1
azure_workspace_id: 0f244ff4-ddd1-468e-8587-933a54a1ef07
columns: ["method", "status", "count"]
query: |
  AzureDiagnostics
  | where Category == "FrontdoorAccessLog"
  | where TimeGenerated > ago(10m)
  | summarize RequestCount = count() by HTTPMethod = httpMethod_s, StatusCode = httpStatusCode_s
  | top 12 by RequestCount
```

## Screenshots

<img class="screenshot" src="/assets/modules/azure_logs.png" width="245" height="254" alt="Azure Logs screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="title", desc="Title to display above the results", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

         {% with name="queryFile", desc="Path to file containing the kusto query", value="." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="azurelogs" %}
{% include "src_path.md" %}
