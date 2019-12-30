---
title: "Resource Usage"
date: 2018-11-12T14:36:08-04:00
draft: false
weight: 190
---

Displays CPU and memory usage.

## Configuration

```yaml
resourceusage:
  cpuCombined: false
  enabled: true
  position:
    top: 1
    left: 1
    height: 1
    width: 1
  refreshInterval: 1
```

## Screenshots

<img class="screenshot" src="/imgs/modules/resource_usage.png" width="279" height="193" alt="resource usage screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/custom name="cpuCombined" desc="_Optional_ Whether or not to display the CPUs as one combined value. Default: `false`." value="true, false" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="resourceusage" %}}