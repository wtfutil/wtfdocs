---
title: "Gerrit"
date: 2018-06-27T15:55:42-07:00
draft: false
weight: 70
---

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

## Screenshots

<img class="screenshot" src="/imgs/modules/gerrit.png" width="640" height="167" alt="gerrit screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/rows >}}
  {{< attributes/custom name="domain" desc="Your Gerrit corporate domain." value="A valid URI." >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/password name="Gerrit" desc="Leave this empty to use the `WTF_GERRIT_PASSWORD` environment variable." >}}
  {{< attributes/position >}}
  {{< attributes/custom name="projects" desc="A list of Gerrit project names to fetch data for." >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/username name="Gerrit" >}}
  {{< attributes/verifyServerCert >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected review in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous project" >}}
  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/l desc="Show the next project" >}}
  {{< keyboard/o desc="Open the selected story in the browser" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous project" >}}
  {{< keyboard/arrowFore desc="Show the next project" >}}
  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="gerrit" %}}