---
title: "CDS Status"
date: 2020-02-05T19:35:54-01:00
draft: false
weight: 70
---

Display current [CDS](https://ovh.github.io/cds/) status. This is useful for CDS Administrator only.

<img class="screenshot" src="/imgs/modules/cds_status.png" width="520" alt="CDS Status screenshot" />

## Configuration

```yml
cdsStatus:
  enabled: true
  position:
    top: 0
    left: 0
    height: 3
    width: 2
  refreshInterval: 8
  apiURL: https://api.cds.localhost.local
  token: xxxxxxxxxxxx
```

{{% attributes %}}
  <tr>
    <td>`apiURL`</td>
    <td>Your CDS API URL.</td>
    <td></td>
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

{{% sourcePath module="cds/status" %}}
