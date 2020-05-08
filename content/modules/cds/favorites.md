---
title: "CDS Favorites"
date: 2020-02-05T19:35:54-01:00
draft: false
weight: 20
---

Display runs of you [CDS](https://ovh.github.io/cds/) favorites workflows.

<img class="screenshot" src="/imgs/modules/cds_favorites.png" width="520" alt="CDS Favorites screenshot" />
## Configuration

{{< code lang="yaml" >}}
cdsFavorites:
  enabled: true
  position:
    top: 0
    left: 0
    height: 2
    width: 2
  refreshInterval: 8
  apiURL: https://api.cds.localhost.local
  token: xxxxxxxxxxxx
  hideTags:
  - "git.repository"
  - "git.hash"
  - "triggered_by"
{{< /code >}}

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
  <tr>
    <td>`hideTags`</td>
    <td>A CDS Runs can have many "cds tags". You can hide some tags displayed.</td>
    <td></td>
  </tr>
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/title >}}
{{% /attributes %}}

<<<<<<< HEAD
{{% sourcePath module="cds/favorites" %}}
=======
## Source Code

{{< code lang="bash" >}}
wtf/modules/cds/favorites/
{{< /code >}}
>>>>>>> Fix syntax highlighting
