---
title: "DigitalOcean"
date: 2019-12-13T11:37:11-08:00
draft: false
weight: 63
---

DigitalOcean module displays a list of your DigitalOcean droplets and Kubernetes clusters and allows you to interact with them in these ways:

* Destroy a droplet
* Enable private networking on a droplet
* Reboot a droplet
* Shut down a droplet
* Show info about a droplet

## Configuration

{{< code lang="yaml" >}}
digitalocean:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 4
    left: 2
    width: 2
    height: 2
  refreshInterval: 15
  title: "🦈 DigitalOcean"
{{< /code >}}

With explicit columns defined:

{{< code lang="yaml" >}}
digitalocean:
  apiKey: "p0d13*********************************************c3"
  columns:
    - Name
    - Status
    - Vcpus
    - Disk
    - Memory
    - Region.Slug
  enabled: true
  position:
    top: 4
    left: 2
    width: 2
    height: 2
  refreshInterval: 15
  title: "🦈 DigitalOcean"
{{< /code >}}

## Screenshots

<img src="/imgs/modules/digitalocean.png" class="screenshot" width="320" height="84" alt="digitalocean screenshot" />

<br />

<img src="/imgs/modules/digitalocean_droplet_info.png" class="screenshot" width="320" height="197" alt="digitalocean screenshot" />

{{% attributes %}}
{{< attributes/apikey name="DigitalOcean" link="https://developers.digitalocean.com/documentation/v2/" envvar="WTF_DIGITALOCEAN_API_KEY" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="columns" desc="_Optional_ A list of the droplet attributes to display. Defines the columns displayed in the widget." value="Any publicly-accessible properties on a DigitalOcean [Droplet](https://github.com/digitalocean/godo/blob/main/droplets.go), [Image](https://github.com/digitalocean/godo/blob/main/images.go), [Region](https://github.com/digitalocean/godo/blob/main/regions.go), or [Size](https://github.com/digitalocean/godo/blob/main/sizes.go)." >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/title >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/custom name="?" desc="Displays information about a droplet" >}}
  {{< keyboard/esc desc="Close the modal dialog" >}}
  {{< keyboard/return desc="Display information about a droplet" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/b desc="Reboot a droplet" >}}
  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/p desc="Enable private networking on a droplet" >}}
  {{< keyboard/s desc="Shut down a droplet" >}}
  {{< keyboard/u desc="Clear selection" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}

  {{< keyboard/spacer >}}

  {{< keyboard/ctrlD >}}
{{% /keyboard %}}

{{% sourcePath module="digitalocean" %}}