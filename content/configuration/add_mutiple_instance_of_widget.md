---
title: "Add mutiple instance of widget"
date: 2020-04-26T20:39:16+05:30
draft: false
---

### How to add mutliple instance of the a particular widget.

If you want to add more than one widget of a particular widget type like if you want 2 todo widgets each for
your personal, official list then you can do so by adding type property to the config yml file. below is the example for the same.

```yaml
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
```yaml
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
