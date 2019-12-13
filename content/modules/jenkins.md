---
title: "Jenkins"
date: 2018-06-09T20:53:35-07:00
draft: false
weight: 130
---

Displays Jenkins status of given builds in a project or view.

## Configuration

```yaml
jenkins:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 2
    left: 3
    height: 2
    width: 3
  refreshInterval: 300
  successBallColor: "green"
  jobNameRegex: ^[a-z]+\[[0-9]+\]$
  url: "https://jenkins.domain.com/jenkins/view_url"
  user: "username"
  verifyServerCertificate: true
```

## Screenshots

<img class="screenshot" src="/imgs/modules/jenkins.png" alt="jenkins screenshot" width="320" height="68" />

{{% attributes %}}
  {{< attributes/apikey name="Jenkins" link="https://wiki.jenkins.io/display/JENKINS/Remote+access+API" envvar="WTF_JENKINS_API_KEY" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="jobNameRegex" desc="_Optional_ A regex that filters the jobs shown in the widget. Any jobs matching the regular expression will be shown." value="A valid regex, e.g. `^[a-z]+\[[0-9]+\]$`" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="successBallColor" desc="Changes the default color of successful Jenkins jobs to the color of your choosing." value="Any valid color name, `blue`, `green`, `purple`, `yellow`, etc." >}}
  {{< attributes/custom name="url" desc="The url to your Jenkins project or view." value="A valid URI." >}}
  {{< attributes/custom name="user" desc="Your Jenkins username." value="" >}}
  {{< attributes/verifyServerCert >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected job in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="jenkins" %}}