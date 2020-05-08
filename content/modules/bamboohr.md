---
title: "BambooHR"
date: 2018-05-07T20:17:37-07:00
draft: false
weight: 10
---

Connects to the BambooHR API and displays who will be Away today.

## Configuration

{{< code lang="yaml" >}}
bamboohr:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 900
  subdomain: "testco"
{{< /code >}}

{{% attributes %}}
  {{< attributes/apikey name="BambooHR" link="https://www.bamboohr.com/api/documentation/" envvar="WTF_BAMBOO_HR_TOKEN" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  <tr>
    <td>`subdomain`</td>
    <td>Your <a href="https://www.bamboohr.com/api/documentation/">BambooHR API</a> subdomain name.</td>
    <td>Leave this empty to use the `WTF_BAMBOO_HR_SUBDOMAIN` environment variable.</td>
  </tr>
{{% /attributes %}}

{{% sourcePath module="bamboohr" %}}