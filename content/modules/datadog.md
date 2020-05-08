---
title: "Datadog"
date: 2018-08-18T00:00:00Z
draft: false
weight: 60
---

Connects to the Datadog API and displays alerting modules.

## Configuration


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

{{% attributes %}}
  {{< attributes/apikey name="DataDog" link="https://docs.datadoghq.com/api/" envvar="WTF_DATADOG_API_KEY" >}}
  {{< attributes/custom name="applicationKey" desc="Your DataDog application key" value="Leave this empty to use the `WTF_DATADOG_APPLICATION_KEY` environment variable." >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="monitors" desc="Configuration for the monitors functionality." value="" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="tags" desc="List of tags you want to query monitors by." value="" >}}
  {{< attributes/title >}}
{{% /attributes %}}

{{% sourcePath module="datadog" %}}