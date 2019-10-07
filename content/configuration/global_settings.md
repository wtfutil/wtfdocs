---
title: "Global Settings"
date: 2018-05-16T21:51:23-07:00
draft: false
weight: 5
---

The following top-level global attributes are configurable in `config.yml`.
See this <a href="https://github.com/wtfutil/wtf/blob/master/_sample_configs/sample_config.yml">example config file</a> for more details.

```yaml
wtf:
  colors:
    background: "red"
    border:
      focusable: "darkslateblue"
      focused: "orange"
      normal: "gray"
    checked: "gray"
    highlight:
      fore: "black"
      back: "green"
    text: "white"
    title: "white"
  grid:
    # How _wide_ the columns are, in terminal characters. In this case we have
    # six columns, each of which are 35 characters wide
    columns: [35, 35, 35, 35, 35, 35]

    # How _high_ the rows are, in terminal lines. In this case we have five rows
    # that support ten line of text, one of three lines, and one of four
    rows: [10, 10, 10, 10, 10, 3, 4]
  navigation:
    shortcuts: true
  openFileUtil: "open"
  sigils:
    checkbox:
      checked: "x"
      unchecked: " "
    paging:
      normal: "*"
      selected: "_"
  term: "xterm-256color"
```

### Attributes

{{% attributes %}}
  {{< attributes/colors/background >}}

  <tr>
    <td>`colors.border.focusable`</td>
    <td>The color in which to draw the border of widgets that can accept keyboard focus.</td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color</a> name.</td>
  </tr>
  <tr>
    <td>`colors.border.focused`</td>
    <td>The color in which to draw the border of the widget that currently has keyboard focus.</td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color</a> name.</td>
  </tr>
  <tr>
    <td>`colors.border.normal`</td>
    <td>The color in which to draw the borders of the widgets that cannot accept focus.</td>
    <td>Any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color</a> name.</td>
  </tr>

  <tr>
    <td>`grid.columns`</td>
    <td>An array that defines the widths of all the columns.</td>
    <td>See <a href="https://github.com/rivo/tview/wiki/Grid">tview's Grid</a> for details</td>
  </tr>
  <tr>
    <td>`grid.rows`</td>
    <td>An array that defines the heights of all the rows.</td>
    <td>See <a href="https://github.com/rivo/tview/wiki/Grid">tview's Grid</a> for details</td>
  </tr>

  {{< attributes/custom name="navigation.shortcuts" desc="Whether or not to display the numeric navigation shortcuts in widget titles." value="`true` or `false`." >}}
  {{< attributes/custom name="openFileUtil" desc="Which local utility to use to open a file or URL." value="" >}}
  {{< attributes/custom name="term" desc="Sets a custom value for the terminal type this app runs in. Leave this entry out of the config if you simply want to use your terminal's default setting. **Note:** If an invalid value is provided for this setting, the app will crash with a `terminal entry not found` error." value="Any valid terminal type (ie: vt100, xterm, xterm-256color, ansi, etc.)." >}}
{{% /attributes %}}