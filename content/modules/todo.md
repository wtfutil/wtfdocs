---
title: "Todo"
date: 2018-05-10T12:41:50-07:00
draft:  false
weight: 220
---

<img class="screenshot" src="/imgs/modules/todo.png" width="320" height="388" alt="todo screenshot" />

An interactive todo list.

## Configuration

```yaml
todo:
  checkedIcon: "X"
  colors:
    checked: gray
    highlight:
      fore: "black"
      back: "orange"
  enabled: true
  filename: "todo.yml"
  position:
    top: 2
    left: 2
    height: 2
    width: 1
  refreshInterval: 3600
```

{{% attributes %}}
  {{< attributes/border >}}

  <row>
    <td>`colors.checked`</td>
    <td>The foreground color for checked rows.</td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color</a> name.</td>
  </row>

  {{< attributes/colors/highlight >}}
  {{< attributes/custom name="checkedIcon" desc="_Optional_ The icon used to denote a 'checked' todo item." value="Any displayable unicode character." >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="filename" desc="The name for the todo file." value="Any valid filename, ideally ending in `yml`." >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

## Keyboard Commands

<span class="caption">Key:</span> `[return]` <br />
<span class="caption">Action:</span> Edit the selected item. <br />
<span class="caption">Action:</span> Close the modal item dialog and save changes. <br />

<span class="caption">Key:</span> `[esc]` <br />
<span class="caption">Action:</span> Remove focus from the selected item. <br />
<span class="caption">Action:</span> Close the modal item dialog without saving changes.

<span class="caption">Key:</span> `[space]` <br />
<span class="caption">Action:</span> Check/uncheck the selected item.

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next item in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous item in the list.

<span class="caption">Key:</span> `n` <br />
<span class="caption">Action:</span> Create a new list item.

<span class="caption">Key:</span> `o` <br />
<span class="caption">Action:</span> Opens the todo list file in
whichever text editor is associated with that file type.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next item in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous item in the list.

<span class="caption">Key:</span> `Ctrl-d` <br />
<span class="caption">Action:</span> Delete the selected item.

<span class="caption">Key:</span> `Ctrl-J` <br />
<span class="caption">Action:</span> Move the selected item down the list.

<span class="caption">Key:</span> `Ctrl-K` <br />
<span class="caption">Action:</span> Move the selected item up the list.

{{% sourcePath module="todo" %}}