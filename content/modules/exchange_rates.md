---
title: "Exchange Rates"
date: 2019-12-13T14:22:54-08:00
draft: false
weight: 64
---

Displays exchange rates between various currencies.

## Configuration

{{< code lang="yaml" >}}
exchangerates:
  enabled: true
  focusable: false
  position:
    top: 4
    left: 4
    width: 1
    height: 2
  rates:
    CAD:
      - "USD"
      - "EUR"
    USD:
      - "CAD"
    EUR:
      - "CAD"
  title: "💰 Rates"
{{< /code >}}

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/custom name="rates" desc="A key/value list of currencies to convert between." value="" >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/title >}}
{{% /attributes %}}

{{% sourcePath module="exchangerates" %}}