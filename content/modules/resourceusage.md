---
title: "Resource Usage"
date: 2018-11-12T14:36:08-04:00
draft: false
weight: 240
---

<img class="screenshot" src="/imgs/modules/resource_usage.png" width="279" height="193" alt="resource usage screenshot" />

Added in `v0.4.1`.

Displays cpu and memory usage.

## Source Code

```bash
wtf/resourceusage/
```

## Configuration

```yaml
resourceusage:
  enabled: true
  position:
    top: 1
    left: 1
    height: 1
    width: 1
  refreshInterval: 1
```

### Attributes

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.
