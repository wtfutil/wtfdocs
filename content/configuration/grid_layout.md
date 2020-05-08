---
title: "Grid Layout"
date: 2019-05-05T12:01:04-07:00
draft: false
weight: 10
---

WTF uses the `Grid` layout system from [tview](https://github.com/rivo/tview/blob/master/grid.go) to position widgets
onscreen. It's not immediately obvious how this works, so here's an
explanation:

Think of your terminal screen as a matrix of letter positions, say `100` chrs wide and `58` chrs tall.

Columns breaks up the width of the screen into chunks, each chunk a specified number of characters wide. use

`[10, 10, 10, 10, 10, 10, 10, 10, 10, 10]`

Ten columns that are ten characters wide

Rows break up the height of the screen into chunks, each chunk a specified number of characters tall. If we wanted to have five rows:

`[10, 10, 10, 10, 18]`

The co-ordinate system starts at top-left and defines how wide and tall a widget is. If we wanted to put a 2-col, 2-row widget in the bottom of the screen, we'd position it at:

{{< code lang="yaml" >}}
  top:    4  // top starts in the 4th row
  left:   9  // left starts in the 9th column
  height: 2  // span down rows 4 & 5 (18 characters in size, total)
  width:  2  // span across cols 9 & 10 (20 characters in size, total)
```