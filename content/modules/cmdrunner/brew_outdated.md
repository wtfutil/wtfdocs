---
title: "brew outdated"
date: 2019-08-03T12:39:10-08:00
draft: false
hidden: true
weight: 10
---

Displays a list of all the installed [Homebrew](https://brew.sh) recipes that have an update available for them.

## Config Example

```yaml
brew_outdated:
  args: ["outdated"]
  cmd: "brew"
  enabled: true
  position:
    top: 3
    left: 1
    width: 2
    height: 1
  type: cmdrunner
```

