---
title: "Blockfolio"
date: 2018-06-13T09:29:59-07:00
draft: false
weight: 10
---

Display your Blockfolio crypto holdings.

## Configuration

```yaml
blockfolio:
  colors:
    name: blue
    grows: green
    drop: red
  device_token: "device token"
  displayHoldings: true
  enabled: true
  position:
    top: 3
    left: 1
    width: 1
    height: 1
  refreshInterval: 400
```

## Screenshots

<img class="screenshot" src="/imgs/modules/blockfolio.png" width="320" height="185" alt="blockfolio screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="colors.drop" >}}
  {{< attributes/colors/custom name="colors.grows" >}}
  {{< attributes/colors/custom name="colors.name" >}}

  <tr>
    <td>`device_token`</td>
    <td>See [this gist](https://github.com/bob6664569/blockfolio-api-client) for details on how to get your Blockfolio API token.</td>
    <td></td>
  </tr>

  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="cryptoexchanges/blockfolio" %}}
