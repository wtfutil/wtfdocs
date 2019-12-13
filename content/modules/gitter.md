---
title: "Gitter"
date: 2018-08-02T12:36:08-04:00
draft: false
weight: 110
---

Displays chat messages from Gitter.

## Configuration

```yaml
gitter:
  apiToken: "d23*******************************************3r2"
  enabled: true
  numberOfMessages: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 4
  roomUri: wtfutil/Lobby
  refreshInterval: 300
```

## Screenshots

<img src="/imgs/modules/gitter.png" width="847" height="160" alt="gitter screenshot" />

{{% attributes %}}
  {{< attributes/apiToken name="Gitter" link="https://developer.gitter.im/apps" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="numberOfMessages" desc="_Optional_ Maximum number of _(newest)_ messages to be displayed. Default is `10`." value="Any positive integer" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="roomURI" desc="_Optional_ URI of the room you would like to see the chat messages from. Default is `wtfutil/Lobby`" value="" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="gitter" %}}