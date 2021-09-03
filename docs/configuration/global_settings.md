---
title: "Global Settings"
date: 2018-05-16T21:51:23-07:00
draft: false
weight: 5
---

# Global Settings

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
  exitMessage:
    display: true
    githubAPIKey: "d8....................................ea"
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
  openUrlUtil:
    - "tmux"
    - "new-window"
    - "elinks"
  sigils:
    checkbox:
      checked: "x"
      unchecked: " "
    paging:
      normal: "*"
      selected: "_"
  term: "xterm-256color"
```

## Attributes

<table>
  --8<-- "attributes/table_header.md"

  <tbody>
    --8<-- "attributes/colors/background.html"

    --8<-- "attributes/colors/border/focusable.md"
    --8<-- "attributes/colors/border/focused.md"
    --8<-- "attributes/colors/border/normal.md"

    --8<-- "attributes/global/exit_message/display.md"
    --8<-- "attributes/global/exit_message/github_api_key.md"

    --8<-- "attributes/global/grid/columns.md"
    --8<-- "attributes/global/grid/rows.md"

    --8<-- "attributes/global/nav_shortcuts.md"
    --8<-- "attributes/global/open_file_util.md"
    --8<-- "attributes/global/open_url_util.md"
    --8<-- "attributes/global/term.md"
  </tbody>
</table>