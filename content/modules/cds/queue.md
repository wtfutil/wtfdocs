---
title: "CDS Queue"
date: 2020-02-05T19:35:54-01:00
draft: false
weight: 50
---

Display current [CDS](https://ovh.github.io/cds/) queue - waiting or building jobs.

<img class="screenshot" src="/imgs/modules/cds_queue.png" width="520" alt="CDS Queue screenshot" />


## Configuration

{{< code lang="yaml" >}}
cdsQueue:
  enabled: true
  position:
    top: 0
    left: 0
    height: 3
    width: 2
  refreshInterval: 8
  apiURL: https://api.cds.localhost.local
  token: xxxxxxxxxxxx
{{< /code >}}

{{% attributes %}}
  <tr>
    <td>`apiURL`</td>
    <td>Your CDS API URL.</td>
    <td>Consumer token scope used: RUN</td>
  </tr>
  <tr>
    <td>`token`</td>
    <td>Your CDS Consumer Token.</td>
    <td></td>
  </tr>
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/title >}}
{{% /attributes %}}

<<<<<<< HEAD
{{% sourcePath module="cds/queue" %}}
=======
## Source Code

{{< code lang="bash" >}}
wtf/modules/cds/queue/
{{< /code >}}
>>>>>>> Fix syntax highlighting
