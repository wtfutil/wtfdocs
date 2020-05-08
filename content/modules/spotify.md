---
title: "Spotify"
date: 2018-10-02T17:13:11-07:00
draft: false
weight: 205
---

Control the Spotify client.

## Configuration

{{< code lang="yaml" >}}
spotify:
  enabled: true
  colors:
    label: "green"
    text: "white"
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 0
{{< /code >}}

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="colors.label" desc="_Optional_ The color for labels. Default: green." >}}
  {{< attributes/colors/custom name="colors.text" desc="_Optional_ The color for text. Default: white." >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected item in the browser" >}}
  {{< keyboard/space desc="Play/pause the currently-selected" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Play previous song" >}}
  {{< keyboard/l desc="Play next song" >}}
  {{< keyboard/r >}}
{{% /keyboard %}}

{{% sourcePath module="spotify" %}}
