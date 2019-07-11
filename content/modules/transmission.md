---
title: "Transmission"
date: 2019-06-25T23:56:08-04:00
draft: false
weight: 235
---

<img class="screenshot" src="/imgs/modules/transmission.png" width="320" height="190" alt="transmission screenshot" />

View and manage your [Transmission](https://transmissionbt.com) bittorrent daemon. This widget shows you the currently-loaded 
torrents, their "download complete" percentage, and their seeding status.

## Configuration

```yaml
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
```

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

## Keyboard Commands

<span class="caption">Key:</span> `[return]` <br />
<span class="caption">Action:</span> Pause/unpause the selected torrent.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next torrent in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous torrent in the list.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Refresh the data.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next torrent in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous torrent in the list.

<span class="caption">Key:</span> `Ctrl-d` <br />
<span class="caption">Action:</span> Delete the selected torrent. This is a non-destructive operation. It removes the torrent from Transmission, it does not remove files from the file system.

{{% sourcePath module="transmission" %}}