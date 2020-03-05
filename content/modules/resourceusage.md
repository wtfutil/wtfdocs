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
  {{< attributes/custom name="showCPU" desc="_Optional_ Whether or not to display the CPU usage. Default: `true`." value="true, false" >}}
  {{< attributes/custom name="cpuCombined" desc="_Optional_ Whether or not to display the CPUs as one combined value. Default: `false`." value="true, false" >}}
  {{< attributes/custom name="showMem" desc="_Optional_ Whether or not to display the memory usage. Default: `true`." value="true, false" >}}
  {{< attributes/custom name="showSwp" desc="_Optional_ Whether or not to display the swap memory usage. Default: `true`." value="true, false" >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="graphIcon" desc="_Optional_ The character to use to display stars in the graph. Default: `|`." value="Any visible alphanumeric character (but emoji will probably break it)." >}}
  {{< attributes/custom name="graphStars" desc="_Optional_ The maximum number of stars to display in the graph. Default: `20`." value="Any positive integer." >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="resourceusage" %}}