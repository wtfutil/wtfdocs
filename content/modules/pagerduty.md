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

### Attributes

`apiKey` <br />
Value: Your <a href="https://v2.developer.pagerduty.com/docs/authentication">PagerDuty API</a> key.

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`escalationFilter` <br />
An array of schedule names you want to filter on. 

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

`scheduleIDs` <br />
An array of schedule IDs you want to restrict the query to.>

`showIncidents` <br />
Whether or not to list incidents. <br />
Values: true or false

`showSchedules` <br />
Whether or not to show schedules. <br />
Values: true or false

## Source Code

```bash
wtf/modules/pagerduty/
```
