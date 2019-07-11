---
title: "Spotify"
date: 2018-10-02T17:13:11-07:00
draft: false
weight: 205
---

Control the Spotify client.

## Configuration

```yaml
spotify:
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 0
```

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected item in the browser" >}}
  {{< keyboard/space desc="Play/pause the currently-selected" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/custom name="h" desc="Play previous song" >}}
  {{< keyboard/custom name="l" desc="Play next song" >}}
  {{< keyboard/r >}}
{{% /keyboard %}}

{{% sourcePath module="spotify" %}}