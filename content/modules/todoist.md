---
title: "Todoist"
date: 2018-07-05T22:55:55-03:00
draft: false
weight: 230
---

<img class="screenshot" src="/imgs/modules/todoist.png" alt="todoist screenshot" />

Displays all items on specified project.

## Configuration

```yaml
todoist:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  position:
    top: 0
    left: 2
    height: 1
    width: 1
  projects:
    - 122247497
  refreshInterval: 3600
```

{{% attributes %}}
  {{< attributes/apikey name="Todoist" link="https://developer.todoist.com/sync/v7/" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/custom name="projects" desc="The todoist projects to fetch items from." value="The integer ID of the project" >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/esc desc="Remove focus from the selected item" >}}
  {{< keyboard/esc desc="Close the modal item dialog without saving changes" >}}
  {{< keyboard/return desc="Edit the selected item" >}}
  {{< keyboard/return desc="Close the modal item dialog and save changes" >}}
  {{< keyboard/space desc="Check/uncheck the selected item" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/c desc="Close current item" >}}
  {{< keyboard/d desc="Delete current item" >}}
  {{< keyboard/h desc="Show the previous project" >}}
  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/l desc="Show the next project" >}}
  {{< keyboard/n desc="Create a new list item" >}}
  {{< keyboard/o desc="Opens the todo list file in whichever text editor is associated with that file type" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
  {{< keyboard/arrowBack desc="Show the previous project" >}}
  {{< keyboard/arrowFore desc="Show the next project" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/custom name="Ctrl-j" desc="Move the selected item down the list" >}}
  {{< keyboard/custom name="Ctrl-k" desc="Move the selected item up the list" >}}
{{% /keyboard %}}

{{% sourcePath module="todoist" %}}