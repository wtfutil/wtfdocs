---
title: "OpsGenie"
date: 2018-05-08T20:53:40-07:00
draft: false
weight: 170
---

Shows OpsGenie on-call schedules.

See <a href="https://docs.opsgenie.com/docs/who-is-on-call-api">Who is on Call API</a> for details. 

## Configuration

### Single Schedule

{{< code lang="yaml" >}}
opsgenie:
  apiKey: "p0d13*********************************************c3"
  displayEmpty: false
  enabled: true
  position:
    top: 2
    left: 1
    height: 2
    width: 1
  refreshInterval: 21600
  region: "us"
  schedule: "Primary"
  scheduleIdentifierType: "id"
{{< /code >}}

### Multiple Schedules

{{< code lang="yaml" >}}
opsgenie:
  apiKey: "p0d13*********************************************c3"
  displayEmpty: false
  enabled: true
  position:
    top: 2
    left: 1
    height: 2
    width: 1
  refreshInterval: 21600
  region: "us"
  schedule:
  - "Primary"
  - "Secondary"
  scheduleIdentifierType: "id"
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/opsgenie.png" width="320" height="389" alt="opsgenie screenshot" />

{{% attributes %}}
  {{< attributes/apikey name="OpsGenie" link="https://docs.opsgenie.com/docs/api-integration" envvar="WTF_OPS_GENIE_API_KEY" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="displayEmpty" desc="Whether schedules with no assigned person on-call should be displayed." value="true, false" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="region" desc="The region of the servers to connect to" value="`eu` or `us`" >}}
  {{< attributes/custom name="scheduleIdentifierType" desc="Type of the schedule identifier." value="`id` or `name`" >}}
{{% /attributes %}}

{{% sourcePath module="opsgenie" %}}