---
title: "New Relic"
date: 2018-05-09T09:01:14-07:00
draft: false
weight: 160
---

Connects to the New Relic API and displays the last n deploys of the
monitored applications: deploy ID, deploy time, and who deployed it.

## Configuration

{{< code lang="yaml" >}}
newrelic:
  apiKey: "p0d13*********************************************c3"
  applicationIDs:
    - 10549735
    - 499785
  deployCount: 6
  enabled: true
  position:
    top: 4
    left: 3
    height: 1
    width: 2
  refreshInterval: 900
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/newrelic.png" width="640" height="189" alt="newrelic screenshot" class="clearfix" />

{{% attributes %}}
  {{< attributes/apikey name="New Relic" link="https://docs.newrelic.com/docs/apis/getting-started/intro-apis/access-rest-api-keys" envvar="WTF_NEW_RELIC_API_KEY" >}}
  {{< attributes/custom name="applicationIds" desc="A list of integer IDs of the New Relic applications you wish to report on." value="Any positive integer." >}}
  {{< attributes/border >}}
  {{< attributes/custom name="deployCount" desc="The number of past deploys to display on screen." value="Any positive integer." >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/arrowBack desc="Show the previous application." >}}
  {{< keyboard/arrowFore desc="Show the next application." >}}
{{% /keyboard %}}

{{% sourcePath module="newrelic" %}}
