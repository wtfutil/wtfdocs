---
title: "BambooHR"
date: 2018-05-07T20:17:37-07:00
draft: false
weight: 10
---

Connects to the BambooHR API and displays who will be Away today.

## Configuration

```yaml
bamboohr:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 900
  subdomain: "testco"
```

{{% attributes %}}
  {{< attributes/apikey name="BambooHR" link="https://www.bamboohr.com/api/documentation/" envvar="WTF_BAMBOO_HR_TOKEN" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

  <tr><td>`subdomain`</td><td>Your <a href="https://www.bamboohr.com/api/documentation/">BambooHR API</a> subdomain name.</td><td></td></tr>
{{% /attributes %}}

{{% sourcePath module="bamboohr" %}}