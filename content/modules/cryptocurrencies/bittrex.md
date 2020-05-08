---
title: "Bittrex"
date: 2018-06-04T20:06:40-07:00
draft: false
weight: 5
---

Get the last 24 hour summary of cryptocurrencies market using [Bittrex](https://bittrex.com).

## Configuration

{{< code lang="yaml" >}}
bittrex:
  colors:
    base:
      name: orange
      displayName: red
    market:
      name: red
      field: white
      value: green
  enabled: true
  position:
    top: -2
    left: 2
    height: 3
    width: 1
  refreshInterval: 5
  summary:
    BTC:
      displayName: Bitcoin
      market:
      - LTC
      - ETH
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/bittrex.png" width="320" height="412" alt="bittrex screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="colors.base.dispayName" >}}
  {{< attributes/colors/custom name="colors.base.name" >}}
  {{< attributes/colors/custom name="colors.market.field" >}}
  {{< attributes/colors/custom name="colors.market.name" >}}
  {{< attributes/colors/custom name="colors.market.value" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

<<<<<<< HEAD
{{% sourcePath module="cryptoexchanges/bittrex" %}}
=======
## Source Code

{{< code lang="bash" >}}
wtf/modules/cryptoexchanges/bittrex/
{{< /code >}}
>>>>>>> Fix syntax highlighting
