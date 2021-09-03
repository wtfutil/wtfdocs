---
title: "IP-API"
date: 2018-06-10T19:41:52-04:00
draft: false
weight: 10
---

Displays your current IP address information, from [IP-APIcom](http://ip-api.com).

**Note:** IP-API.com has a free-plan rate limit of 120 requests per
minute.

## Configuration

{{< code lang="yaml" >}}
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
{{< /code >}}

{{% attributes %}}
  {{< attributes/border >}}

  {{< attributes/colors/custom name="colors.name" desc="_Optional_ The default colour for the row names. Default: red." >}}
  {{< attributes/colors/custom name="colors.value" desc="_Optional_ The default colour for the row values. Default: white." >}}
  
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="ipapi" %}}