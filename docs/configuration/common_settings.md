---
title: "Common Settings"
date: 2019-09-22T18:20:35-07:00
draft: false
weight: 7
---

# Common Settings

The following settings are common to all modules. Common settings have logical defaults and are all optional. An explicitly-defined common setting will over-ride a module's internal default setting value.

An example with all common settings explicitly configured.

```yaml
feedreader:
  border: true
  enabled: true
  feeds:
  - https://news.ycombinator.com/rss
  feedLimit: 10
  focusable: false
  focusChar: 2
  position:
    top: 2
    left: 2
    width: 1
    height: 1
  title: "Hacker News"
  refreshInterval: 14400
```

## Attributes

<table>
  --8<-- "attributes/table_header.md"

  <tbody>
    --8<-- "attributes/border.md"
    --8<-- "attributes/enabled.md"
    --8<-- "attributes/focusable.md"
    --8<-- "attributes/focus_char.md"
    --8<-- "attributes/position.md"
    --8<-- "attributes/refreshInterval.md"
    --8<-- "attributes/title.md"
  </tbody>
</table>