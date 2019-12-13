---
title: "Rollbar"
date: 2019-02-13T14:36:08-04:00
draft: false
weight: 202
---

Displays item information for your rollbar account.

## Configuration

```yaml
rollbar:
  accessToken: "abjsdfoia7sdg8fy7g"
  enabled: true
  projectOwner: "ENCOM"
  projectName: "MCP"
  activeOnly: true
  assignedToName: "dillinger"
  count: 3
  position:
    top: 4
    left: 1
    height: 2
    width: 2
  refreshInterval: 900
```

## Screenshots

<img class="screenshot" src="/imgs/modules/rollbar.png" width="640" height="187" alt="rollbar screenshot" />

{{% attributes %}}
  {{< attributes/custom name="accessToken" desc="Your Rollbar project access token (only needs read capabilities)." value="" >}}
  {{< attributes/custom name="activeOnly" desc="Only show items that are active." value="true, false" >}}
  {{< attributes/custom name="assignedToName" desc="Set this to your username if you only want to see items assigned to you." value="A string of your username" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="count" desc="How many items you want to see. 100 is max." value="Any positive integer up to 100 inclusive." >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/custom name="projectName" desc="This is used to create a link to the item" value="" >}}
  {{< attributes/custom name="projectOwner" desc="This is used to create a link to the item" value="" >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected item in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="rollbar" %}}