---
title: "ARPANSA"
date: 2018-05-09T11:44:13-07:00
draft: false
weight: 5
---

<img class="screenshot" src="/imgs/modules/arpansa.png" width="350" height="150" alt="arpansagovau module screenshot" />

Displays Ultraviolet radiation index information from ARPANSA for an Australian city to help determine what level of sun protection or avoidance is necessary.

The [Australian Radiation Protection and Nuclear Safety Agency](https://www.arpansa.gov.au) (ARPANSA) is the Australian Government's primary authority on radiation protection and nuclear safety.

Interpreting the information:

* Index is specified in units of [Standard Erthermal Dose](https://www.arpansa.gov.au/services/monitoring/ultraviolet-radiation-monitoring/ultraviolet-radiation-dose/ultraviolet).
* If the UV index is less than 3 you can safely stay outdoors with minimal protection.
* If the UV index is 3 or more: wear sun protective clothing, a hat, sunglasses, sunscreen, seek shade.

## Configuration

{{< code lang="yaml" >}}
    arpansagovau:
      enabled: true
      locationid: "Sydney"
      refreshInterval: 900
      position:
        top: 0
        left: 0
        height: 1
        width: 1
{{< /code >}}

{{% attributes %}}
  <tr>
    <td>`locationid`</td>
    <td>One of the <a href="https://uvdata.arpansa.gov.au/xml/uvvalues.xml">ARPANSA location ids as seen on the id attribute of the location tag. e.g. "Sydney"</td>
  </tr>

  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

{{% /attributes %}}

{{% sourcePath module="weatherservices/arpansagovau" %}}
