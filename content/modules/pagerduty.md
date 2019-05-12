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
    - <Schedules you care about>
  position:
    top: 4
    left: 3
    height: 1
    width: 2
  showIncidents: true
  showSchedules: true
```

### Attributes

`apiKey` <br />
Value: Your <a href="https://v2.developer.pagerduty.com/docs/authentication">PagerDuty API</a> key.

`escalationFilter` <br />
Array of schedules you want to filter on.

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`escalationFilter` <br />

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

`showIncidents` <br />
Whether or not to list incidents. <br />
Values: true or false

`showSchedules` <br />
Whether or not to show schedules. <br />
Values: true or false

## Source Code

```bash
wtf/pagerduty/
```
