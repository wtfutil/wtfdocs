---
title: "Pagerduty"
date: 2018-08-18T00:00:00Z
draft: false
weight: 175
---

Connects to the Pagerduty API and shows schedules

## Configuration

```yaml
pagerduty:
  apiKey: "<yourapikey>"
  enabled: true
  escalationFilter:
  - "client-eng"
  position:
    top: 4
    left: 3
    height: 1
    width: 2
  scheduleIDs:
  - "R2D24CD"
  - "C3P05MF"
  showIncidents: true
  showSchedules: true
```

{{% attributes %}}
  {{< attributes/apikey name="PagerDuty" link="https://v2.developer.pagerduty.com/docs/authentication" envvar="WTF_PAGERDUTY_API_KEY" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="escalationFilter" desc="An array of schedule names you want to filter on." value="" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="scheduleIDs" desc="An array of schedule IDs you want to restrict the query to." value="" >}}
  {{< attributes/custom name="showIncidents" desc="_Optional_ Whether or not to list incidents. Default: true." value="true, false" >}}
  {{< attributes/custom name="showSchedules" desc="_Optional_ Whether or not to show schedules. Default: true." value="true, false" >}}
{{% /attributes %}}

{{% sourcePath module="pagerduty" %}}