---
title: "NBA Score"
date: 2019-03-07T05:32:11-07:00
draft: false
weight: 158
---

Displays NBA game scores.

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Go to previous day

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Go to next day

<span class="caption">Key:</span> `c` <br />
<span class="caption">Action:</span> Go back to current day

## Configuration

```yaml
nbascore:
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 600
```

## Attributes

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`focusChar` <br />
Define one of the number keys as a short cut key to access the widget. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.


## Source Code

```bash
wtf/modules/modules/nbascore/
```
