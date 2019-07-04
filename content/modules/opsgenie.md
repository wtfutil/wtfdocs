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

### Attributes

`apiKey` < br />
Value: Your <a href="https://docs.opsgenie.com/docs/api-integration">OpsGenie API</a> token.

`displayEmpty` <br />
Whether schedules with no assigned person on-call should be displayed. <br />
Values:  `true`, `false`.

`enabled` <br />
Whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

`schedule` <br />
The name or list of names of the schedule(s) to retrieve. <br />

`scheduleIdentifierType` <br />
Type of the schedule identifier. <br />
Values: `id` or `name`.


## Source Code

```bash
wtf/modules/opsgenie/
```
