---
title: "CryptoLive"
date: 2018-06-03T20:06:40-07:00
draft: false
weight: 15
---

Compare crypto currencies using [CryptoCompare](https://cryptocompare.com).

## Configuration

{{< code lang="yaml" >}}
cryptolive:
  enabled: true
  position:
    top: 5
    left: 2
    height: 1
    width: 2
  updateInterval: 15
  currencies:
    BTC:
      displayName: Bitcoin
      to:
        - USD
        - EUR
        - ETH
        - LTC
        - DOGE
    LTC:
      displayName: Ethereum
      to:
        - USD
        - EUR
        - BTC
  top:
    BTC:
      displayName: Bitcoin
      limit: 5
      to:
        - USD
  colors:
    from:
      name: coral
      displayName: grey
    to:
      name: white
      price: green
    top:
      from:
        name: grey
        displayName: coral
      to:
        name: red
        field: white
        value: green
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/cryptolive.png" width="320" height="203" alt="cryptolive screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="colors.from.displayName" >}}
  {{< attributes/colors/custom name="colors.from.name" >}}
  {{< attributes/colors/custom name="colors.to.name" >}}
  {{< attributes/colors/custom name="colors.to.price" >}}
  {{< attributes/custom name="currencies" desc="" value="" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="cryptoexchanges/cryptolive" %}}
