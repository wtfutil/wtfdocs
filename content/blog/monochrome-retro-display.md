---
title: "Monochrome Retro Display"
date: 2019-11-10T11:43:32-08:00
draft: false
---

{{< publishedDate >}}

With v0.24.0, WTF now has better support for theme-like colour settings. It's far from perfect, a lot of modules will have to be improved internally to make theming ubiquitous, but it's a start.

By way of example, if you're running v0.24 or later, drop this into your config at the top, replace your existing `colors:` YAML block with the following and you'll end up with a facsimile of an old-school green monochrome monitor display (you may need to restart WTF to get changes to take effect).

```yaml
  colors:
    background: "transparent"
    border:
      focusable: "lightgreen"
      focused: "goldenrod"
      normal: "darkgreen"
    checked: "gray"
    highlight:
      fore: "black"
      back: "green"
    labels: "lightgreen::b"
    rows:
      even: "green"
      odd: "lightgreen"
    subheading: "lightgreen::b"
    text: "green"
    title: "lightgreen"
```