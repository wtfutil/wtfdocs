---
title: "iStats"
date: 2019-07-01T17:17:10-04:00
draft: false
hidden: true
weight: 40
---

[iStats](https://github.com/Chris911/iStats) is a command line tool to view
system stats on OSX.

<img class="screenshot" src="/imgs/modules/cmdrunner/iStats.png" alt="istats screenshot" />

## Config Example

{{< code lang="yaml" >}}
istats:
  args: ["all"]
  cmd: "istats"
  enabled: true
  type: "cmdrunner"
  position:
    top: 0
    left: 3
    height: 2
    width: 2
  refreshInterval: 1
{{< /code >}}

