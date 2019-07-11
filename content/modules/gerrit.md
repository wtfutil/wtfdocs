---
title: "Gerrit"
date: 2018-06-27T15:55:42-07:00
draft: false
weight: 70
---

<img class="screenshot" src="/imgs/modules/gerrit.png" width="640" height="167" alt="gerrit screenshot" />

Displays information about your projects hosted on Gerrit:

#### Open Incoming Reviews

All open reviews that are requesting your approval.

#### My Outgoing Reviews

All open reviews created by you.

## Configuration

```yaml
gerrit:
  colors:
    rows:
      even: "lightblue"
      odd: "white"
  domain: https://gerrit-review.googlesource.com
  enabled: true
  password: "mypassword"
  position:
    top: 2
    left: 3
    height: 2
    width: 2
  projects:
  - org/test-project"
  - dotfiles
  refreshInterval: 300
  username: "myname"
  verifyServerCertificate: false
```

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/rows >}}
  {{< attributes/custom name="domain" desc="Your Gerrit corporate domain." value="A valid URI." >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/password name="Gerrit" >}}
  {{< attributes/position >}}
  {{< attributes/custom name="projects" desc="A list of Gerrit project names to fetch data for." >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/username name="Gerrit" >}}
  {{< attributes/verifyServerCert >}}
{{% /attributes %}}

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Show the previous project.

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Show the next project.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next review in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous review in the list.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Refresh the data.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Show the previous project.

<span class="caption">Key:</span> `→` <br />
<span class="caption">Action:</span> Show the next project.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next review in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous review in the list.

<span class="caption">Key:</span> `[return]` <br />
<span class="caption">Action:</span> Open the selected review in the browser.


{{% sourcePath module="gerrit" %}}