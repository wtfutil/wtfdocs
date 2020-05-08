---
title: "Adding Multiple Instances of a Widget"
date: 2020-04-26T20:39:16+05:30
draft: false
---

### How to add multiple instances of a widget

To add more than one instance of a particular widget, for example, if you want two Todo widgets, you can do so by adding the `type` property to the entries in your `config.yml` file. Below is an example for Todo:

{{< code lang="yaml" >}}
todo1:
  checkedIcon: "X"
  colors:
    checked: gray
    highlight:
      fore: "black"
      back: "orange"
  enabled: true
  filename: "todo.yml"
  position:
    top: 0
    left: 0
    height: 2
    width: 2:wq
  refreshInterval: 3600
  type: todo
```

{{< code lang="yaml" >}}
todo2:
  checkedIcon: "X"
  colors:
    checked: gray
    highlight:
      fore: "black"
      back: "orange"
  enabled: true
  filename: "todo.yml"
  position:
    top: 0
    left: 2
    height: 2
    width: 2
  refreshInterval: 3600
  type: todo
```
