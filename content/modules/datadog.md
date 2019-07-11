---
title: "Datadog"
date: 2018-08-18T00:00:00Z
draft: false
weight: 60
---

Connects to the Datadog API and displays alerting modules.

## Configuration

```yaml
datadog:
  apiKey: "<yourapikey>"
  applicationKey: "<yourapplicationkey>"
  enabled: true
  monitors:
    tags:
      - "team:ops"
  position:
    top: 4
    left: 3
    height: 1
    width: 2
```

{{% attributes %}}
  {{< attributes/apikey name="DataDog" link="https://docs.datadoghq.com/api/" >}}
  {{< attributes/custom name="applicationKey" description="Your DataDog application key" value="" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="monitors" description="Configuration for the monitors functionality." value="" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="tags" description="List of tags you want to query monitors by." value="" >}}
{{% /attributes %}}

{{% sourcePath module="datadog" %}}