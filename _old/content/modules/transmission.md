---
title: "Transmission"
date: 2019-06-25T23:56:08-04:00
draft: false
weight: 235
---

View and manage your [Transmission](https://transmissionbt.com) bittorrent daemon. This widget shows you the currently-loaded 
torrents, their "download complete" percentage, and their seeding status.

## Configuration

{{< code lang="yaml" >}}
transmission:
  enabled: true
  host: "192.168.1.5"
  password: "passwordpassword"
  position:
    top: 4
    left: 3
    width: 2
    height: 1
  refreshInterval: 3
  username: "transmission"
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/transmission.png" width="320" height="190" alt="transmission screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="host" desc="The IP address of the machine that your Transmission daemon is running on." value="" >}}
  {{< attributes/custom name="password" desc="The password you use to connect to your Transmission daemon." value="" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="username" desc="The username you use to connect to your Transmission daemon." value="" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Pause/unpause the selected torrent" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}

  {{< keyboard/spacer >}}

  {{< keyboard/custom name="Ctrl-d" desc="Delete the selected torrent. This is a non-destructive operation. It removes the torrent from Transmission, it does not remove files from the file system" >}}
{{% /keyboard %}}

{{% sourcePath module="transmission" %}}