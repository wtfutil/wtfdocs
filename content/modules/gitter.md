---
title: "Gitter"
date: 2018-08-02T12:36:08-04:00
draft: false
weight: 110
---

<img src="/imgs/modules/gitter.png" width="847" height="160" alt="gitter screenshot" />

Displays chat messages from Gitter.

## Configuration

```yaml
gitter:
  apiToken: "ab345546asdfasb465234fgjgh068f39a35c3e4139ee383f7"
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

{{% attributes %}}
  {{< attributes/apiToken name="Gitter" link="https://developer.gitter.im/apps" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="numberOfMessages" desc="_Optional_ Maximum number of _(newest)_ messages to be displayed. Default is `10`." value="Any positive integer" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="roomURI" desc="_Optional_ URI of the room you would like to see the chat messages from. Default is `wtfutil/Lobby`" value="`new`, `top`, `job`, `ask`" >}}
{{% /attributes %}}

## Keyboard Commands

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next message in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous message in the list.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Refresh the data.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next message in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous message in the list.


{{% sourcePath module="gitter" %}}