---
title: "Rollbar"
date: 2019-02-13T14:36:08-04:00
draft: false
weight: 202
---

<img class="screenshot" src="/imgs/modules/rollbar.png" width="640" height="187" alt="rollbar screenshot" />


Displays item information for your rollbar account.

## Keyboard Commands

<span class="caption">Key:</span> `[return]` <br />
<span class="caption">Action:</span> Open the selected item in the browser.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next item in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous item in the list.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Refresh the data.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next item in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous item in the list.

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

### Attributes

`accessToken` <br />
Value: Your Rollbar project access token(Only needs read capabilities).

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`projectOwner` <br />
This is used to create a link to the item <br />
Values: A string of project owners name.

`projectName` <br />
This is used to create a link to the item <br />
Values: A string of the projects name

`activeOnly` <br />
Only show items that are active <br />
Values: `true`, `false`.

`assignedToName` <br />
Set this to your username if you only want to see items assigned to you <br />
Values: A string of your user_name

`count` <br />
How many items you want to see. 100 is max <br />
Values: A positive integer, `0..100`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

{{% sourcePath module="rollbar" %}}