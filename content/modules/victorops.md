---
title: "VictorOps OnCall"
date: 2019-01-20T00:28:41-08:00
draft: false
weight: 265
---

Connects to the VictorOps API and determines who is on call

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
  refreshInterval: 3600
  team: devops
```

{{% attributes %}}
  <tr>
    <td>`apiID`</td>
    <td>Your <a href="https://help.victorops.com/knowledge-base/api/">VictorOps API ID</a> token.</td>
    <td></td>
  </tr>

  {{< attributes/apikey name="VictorOps" link="https://help.victorops.com/knowledge-base/api/" envvar="WTF_VICTOROPS_API_KEY" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="team" desc="_Optional_ Whether or not to only show a specific team. Default: all teams are shown." value="The team slug that can be found in the URL after `/#/team/`" >}}
{{% /attributes %}}

{{% sourcePath module="victorops" %}}