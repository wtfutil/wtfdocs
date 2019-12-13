---
title: "IPInfo"
date: 2018-06-01T23:18:48-07:00
draft: false
weight: 20
---

Displays your current IP address information, from ipinfo.io.

**Note:** IPInfo.io has a free-plan rate limit of 1000 requests per day.

## Configuration

```yaml
ipinfo:
  colors:
    name: red
    value: white
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 150
```

## Screenhots

<img class="screenshot" src="/imgs/modules/ipinfo.png" width="320" height="199" alt="ipinfo screenshot" />

{{% attributes %}}
  {{< attributes/border >}}

  {{< attributes/colors/custom name="colors.name" desc="_Optional_ The default colour for the row names. Default: red." >}}
  {{< attributes/colors/custom name="colors.value" desc="_Optional_ The default colour for the row values. Default: white." >}}
  
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="ipinfo" %}}