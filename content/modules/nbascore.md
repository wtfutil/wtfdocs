---
title: "NBA Score"
date: 2019-03-07T05:32:11-07:00
draft: false
weight: 158
---

Displays NBA game scores.

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
{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Go to previous day

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Go to next day

<span class="caption">Key:</span> `c` <br />
<span class="caption">Action:</span> Go back to current day

{{% sourcePath module="nbascore" %}}