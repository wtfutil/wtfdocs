---
title: "Textfile"
date: 2018-05-09T11:13:11-07:00
draft: false
weight: 210
---

Displays the contents of the specified text file in the widget.

## Configuration

```yaml
textfile:
  enabled: true
  filePaths:
  - "~/Desktop/notes.md"
  - "~/.config/wtf/config.yml"
  format: true
  formatStyle: "dracula"
  position:
    top: 5
    left: 4
    height: 2
    width: 1
  refreshInterval: 15
  wrapText: true
```

## Screenshots

<img class="screenshot" src="/imgs/modules/textfile.png" width="320" height="133" alt="textfile screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="filePaths" desc="An array of paths to the files to be displayed in the widget." value="" >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="format" desc="_Optional_ Whether or not to try and format and syntax highlight the displayedtext. Default: false." value="true, false" >}}

  <tr>
    <td>`formatStyle`</td>
    <td>_Optional_ The style of syntax highlighting to format the text with. Default: `vim`.</td>
    <td>See [Chroma styles](https://github.com/alecthomas/chroma/tree/master/styles) for all valid options.</td>
  </tr>

  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/wrapText >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open current file" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Select previous file" >}}
  {{< keyboard/l desc="Select next file" >}}
  {{< keyboard/o desc="Opens the text file in whichever text editor is associated  with that file type" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Select previous file" >}} 
  {{< keyboard/arrowFore desc="Select next file" >}} 
{{% /keyboard %}}

{{% sourcePath module="textfile" %}}