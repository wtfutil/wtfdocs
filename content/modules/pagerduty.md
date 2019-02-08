---
title: "Pagerduty"
date: 2018-08-18T00:00:00Z
draft: false
weight: 60
---

Connects to the Pagerduty API and shows schedules

## Configuration

```yaml
pagerDuty:
  apiKey: "<yourapikey>"
  enabled: true
  escalationFilter:
    - <Schedules you care about>
  position:
    top: 4
    left: 3
    height: 1
    width: 2
```

### Attributes

`apiKey` <br />
Value: Your <a href="https://v2.developer.pagerduty.com/docs/authentication">PagerDuty API</a> key.

`escalationFilter` <br />
Array of schedules you want to filter on.

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

## Source Code

```bash
wtf/pagerduty/
```
