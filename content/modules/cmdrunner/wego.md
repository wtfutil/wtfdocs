---
title: "wego"
date: 2019-10-12T17:17:10-04:00
draft: false
hidden: true
weight: 40
---

[wego](https://github.com/schachmat/wego) is a command line tool to view
weather, from a variety of weather services

<img class="screenshot" src="/imgs/modules/cmdrunner/wego.png" alt="wego screenshot" />

## Config Example

```yaml
weather:
  args: ["0"]
  cmd: "wego"
  enabled: true
  type: "cmdrunner"
  position:
    top: 0
    left: 0
    height: 1
    width: 2
  refreshInterval: 100
```
