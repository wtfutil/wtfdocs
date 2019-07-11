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

## Keyboard Commands

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Show the previous project.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Show the previous project.

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Show the next project.

<span class="caption">Key:</span> `→` <br />
<span class="caption">Action:</span> Show the next project.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next item in the list.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next item in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous item in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous item in the list.

<span class="caption">Key:</span> `c` <br />
<span class="caption">Action:</span> Close current item.

<span class="caption">Key:</span> `d` <br />
<span class="caption">Action:</span> Delete current item.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Reload all projects.

{{% sourcePath module="todoist" %}}