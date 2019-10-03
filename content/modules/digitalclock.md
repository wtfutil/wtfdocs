---
title: "Digital Clock"
date: 2019-09-10T09:57:28-07:00
draft: false
weight: 61
---

<img src="/imgs/modules/digitalclock.png" class="screenshot" width="240" height="121" alt="digitalclock screenshot" />

Displays a configurable digital clock.

## Configuration

```yaml
digitalclock:
  color: orange
  enabled: true
  font: bigfont
  hourFormat: 12
  position:
    top: 0
    left: 1
    height: 1
    width: 1
  refreshInterval: 1
  title: "big clock"
  type: "digitalclock"
```

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="color" desc="The color to display the clock time in." >}}
  {{< attributes/custom name="font" desc="The font to display the clock time in." value="`bigfont` or `digitalfont`" >}}
  {{< attributes/enabled >}}
  {{< attributes/hourFormat >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="digitalclock" %}}