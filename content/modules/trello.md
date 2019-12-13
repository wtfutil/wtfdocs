---
title: "Trello"
date: 2018-05-10T10:44:35-07:00
draft: false
weight: 250
---

Displays all Trello cards on specified lists.

## Configuration

### Single Trello List

```yaml
trello:
  accessToken: "7b8b14f8743a408a93276d7155dd9ee2"
  apiKey: "p0d13*********************************************c3"
  board: Main
  enabled: true
  list: "Todo"
  position:
    height: 1
    left: 2
    top: 0
    width: 1
  refreshInterval: 3600
  username: myname
```

### Multiple Trello Lists

If you want to monitor multiple Trello lists, use the following
configuration (note the difference in `list`):

```yaml
trello:
  accessToken: "7b8b14f8743a408a93276d7155dd9ee2"
  apiKey: "p0d13*********************************************c3"
  board: Main
  enabled: true
  list: ["Todo", "Done"]
  position:
    height: 1
    left: 2
    top: 0
    width: 1
  refreshInterval: 3600
  username: myname
```

## Screenshots

<img class="screenshot" src="/imgs/modules/trello.png" width="640" height="197" alt="trello screenshot" />

{{% attributes %}}
  {{< attributes/apikey name="Trello" link="" envvar="WTF_TRELLO_APP_KEY" >}}
  {{< attributes/custom name="accessToken" desc="Your Trello access token." >}}
  {{< attributes/custom name="board" desc="The name of the Trello board." >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="list" desc="The Trello lists to fetch cards from." >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/username name="Trello" >}}
{{% /attributes %}}

{{% sourcePath module="trello" %}}