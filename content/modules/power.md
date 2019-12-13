---
title: "Power"
date: 2018-05-26T19:26:23-07:00
draft: false
weight: 180
---

Displays information about the current power source.

For battery, also displays the current charge, estimated time remaining, and whether it is charging or discharging.

## Configuration

```yaml
power:
  enabled: true
  position:
    top: 5
    left: 0
    height: 2
    width: 1
  refreshInterval: 15
```

## Screenshots

<img class="screenshot" src="/imgs/modules/power.png" width="320" height="129" alt="power screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="power" %}}