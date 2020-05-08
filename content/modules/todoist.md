---
title: "Todoist"
date: 2018-07-05T22:55:55-03:00
draft: false
weight: 230
---

Displays all items on specified project.

## Configuration

{{< code lang="yaml" >}}
todoist:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 0
    left: 2
    height: 1
    width: 1
  projects:
    - 122247497
  refreshInterval: 3600
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/todoist.png" alt="todoist screenshot" />

{{% attributes %}}
  {{< attributes/apikey name="Todoist" link="https://developer.todoist.com/sync/v7/" envvar="WTF_TODOIST_TOKEN" >}}
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

  {{< keyboard/spacer >}}

  {{< keyboard/c desc="Close current item" >}}
  {{< keyboard/d desc="Delete current item" >}}
  {{< keyboard/h desc="Show the previous project" >}}
  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/l desc="Show the next project" >}}
  {{< keyboard/u desc="Clear the current selection" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
  {{< keyboard/arrowBack desc="Show the previous project" >}}
  {{< keyboard/arrowFore desc="Show the next project" >}}

  {{< keyboard/spacer >}}
{{% /keyboard %}}

{{% sourcePath module="todoist" %}}