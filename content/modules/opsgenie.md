---
title: "OpsGenie"
date: 2018-05-08T20:53:40-07:00
draft: false
weight: 170
---

<img class="screenshot" src="/imgs/modules/opsgenie.png" width="320" height="389" alt="opsgenie screenshot" />

Connects to the OpsGenie API and displays all your scheduled rotations
and who's currently on call.

See <a href="https://docs.opsgenie.com/docs/who-is-on-call-api">Who is on Call API</a> for details. 

## Configuration

### Single Schedule

```yaml
opsgenie:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  displayEmpty: false
  enabled: true
  position:
    top: 2
    left: 1
    height: 2
    width: 1
  refreshInterval: 21600
  schedule: "Primary"
  scheduleIdentifierType: "id"
```

### Multiple Schedules

```yaml
opsgenie:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  displayEmpty: false
  enabled: true
  position:
    top: 2
    left: 1
    height: 2
    width: 1
  refreshInterval: 21600
  schedule:
  - "Primary"
  - "Secondary"
  scheduleIdentifierType: "id"
```
{{% attributes %}}
  {{< attributes/apikey name="OpsGenie" link="https://docs.opsgenie.com/docs/api-integration" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="displayEmpty" desc="Whether schedules with no assigned person on-call should be displayed." value="true, false" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="schedule" desc="The name or list of names of the schedule(s) to retrieve." value="" >}}
  {{< attributes/custom name="scheduleIdentifierType" desc="Type of the schedule identifier." value="`id` or `name`" >}}
{{% /attributes %}}

{{% sourcePath module="opsgenie" %}}