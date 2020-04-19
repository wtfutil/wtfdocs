---
title: "Pi-hole"
date: 2019-04-13T17:26:23-01:00
draft: false
weight: 177
---

Displays information about a running [Pi-hole](https://pi-hole.net/) server.

## Configuration

```yaml
pihole:
  enabled: true
  position:
    top: 5
    left: 0
    height: 2
    width: 2
  refreshInterval: 60
  apiUrl: http://192.168.1.100:1010/admin/api.php
  token: atvvedmpyat8140rnhodrok3qr58d8ph85wl6wk1rpb9upiwx1tl6eittz403pqaj
  showSummary: true
  showTopItems: 5
  showTopClients: 5
  maxClientWidth: 20
  maxDomainWidth: 20
```

## Screenshots

<img class="screenshot" src="/imgs/modules/pihole.png" width="688" height="420" alt="Pi-hole screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="apiUrl" desc="The Pi-Hole API Server URL. Typically: http://<ip:port>/admin/api.php" value="" >}}
  {{< attributes/custom name="token" desc="Navigate to http://<ip:port>/admin/settings.php?tab=api and choose \"Show API Token\"." value="" >}}
  {{< attributes/custom name="showSummary" desc="Show summary. Default: `true`." value="true, false" >}}
  {{< attributes/custom name="showTopItems" desc="_Optional_ Number of Top Queries and Top Ads to display. 0 disables the output. Default: `5`." value="Integer" >}}
  {{< attributes/custom name="showTopClients" desc="_Optional_ Number of Top Sources and Query Types to display. 0 disables the output. Default: `5`." value="Integer" >}}
  {{< attributes/custom name="maxClientWidth" desc="_Optional_ Number of characters to display when outputting query and ad domain names. Default: `20`." value="Integer" >}}
  {{< attributes/custom name="maxDomainWidth" desc="_Optional_ Number of characters to display when outputting client name and IP. Default: `20`." value="Integer" >}}

{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/d desc="Disable Pi-hole ad blocking" >}}
  {{< keyboard/e desc="Enable Pi-hole ad blocking" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/r >}}

{{% /keyboard %}}

{{% sourcePath module="pihole" %}}