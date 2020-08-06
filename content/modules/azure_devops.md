---
title: "Azure DevOps"
date: 2018-05-07T20:17:37-07:00
draft: false
weight: 5
---

## Configuration

{{< code lang="yaml" >}}
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
{{< /code >}}


{{% attributes %}}
  {{< attributes/apiToken link="https://azure.microsoft.com/en-ca/services/devops/" name="Azure DevOps" envvar="WTF_AZURE_DEVOPS_API_TOKEN" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="labelColor" desc="_Optional_ The color of the title label. Default: `white`." value="Any X11 color name." >}}
  {{< attributes/custom name="maxRows" desc="_Optional_ The maximum number of rows to display. Default: `3`." value="Any positive integer." >}}
  {{< attributes/custom name="orgURL" desc="The URL to your Azure DevOps project." value="Leave empty to use the `WTF_AZURE_DEVOPS_ORG_URL` environment variable." >}}
  {{< attributes/position >}}
  {{< attributes/custom name="projectName" desc="The name of your Azure DevOps project." value="Leave empty to use the `WTF_AZURE_DEVOPS_PROJECT_NAME` environment variable." >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="azuredevops" %}}