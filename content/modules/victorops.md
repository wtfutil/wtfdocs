---
title: "VictorOps OnCall"
date: 2019-01-20T00:28:41-08:00
draft: false
weight: 10
---

Connects to the VictorOps API and determines who is on call

## Configuration

```yaml
victorops:
  apiID: a3c5dd63
  apiKey: 3276d7155dd9ee27b8b14f8743a408a9
  enabled: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 3600
  team: devops
```

### Attributes

`apiID` <br />
Value: Your <a href="https://help.victorops.com/knowledge-base/api/">VictorOps API ID</a> token.

`apiKey` <br />
Value: Your <a href="https://help.victorops.com/knowledge-base/api/">VictorOps API Key</a> token.

`enabled` <br />
Whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: Any positive integer, `0..n`.

`team` <br />
Value: An optional value to only show a specific team. By default, all teams are shown. <br />
Values: The team slug that can be found in the URL after `/#/team/`

## Source Code

```bash
wtf/victorops/
```

