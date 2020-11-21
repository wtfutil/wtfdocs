---
title: "NBA Score"
date: 2019-03-07T05:32:11-07:00
draft: false
weight: 50
---

Displays NBA game scores.

## Configuration

{{< code lang="yaml" >}}
nbascore:
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 600
{{< /code >}}

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/c desc="Go to current day" >}}
  {{< keyboard/h desc="Go to previous day" >}}
  {{< keyboard/l desc="Go to next day" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Go to previous day" >}}
  {{< keyboard/arrowFore desc="Go to next day" >}}
{{% /keyboard %}}

{{% sourcePath module="nbascore" %}}