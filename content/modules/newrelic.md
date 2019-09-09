---
title: "New Relic"
date: 2018-05-09T09:01:14-07:00
draft: false
weight: 160
---

<img class="screenshot" src="/imgs/modules/newrelic.png" width="640" height="189" alt="newrelic screenshot" class="clearfix" />

Connects to the New Relic API and displays the last n deploys of the
monitored applications: deploy ID, deploy time, and who deployed it.

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Show the previous application.

<span class="caption">Key:</span> `→` <br />
<span class="caption">Action:</span> Show the next application.

## Configuration

```yaml
newrelic:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
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
```

{{% attributes %}}
  {{< attributes/apikey name="New Relic" link="https://docs.newrelic.com/docs/apis/getting-started/intro-apis/access-rest-api-keys" envvar="WTF_NEW_RELIC_API_KEY" >}}
  {{< attributes/custom name="applicationId" desc="The integer ID of the New Relic application you wish to report on." value="Any positive integer" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="deployCount" desc="The number of past deploys to display on screen." value="Any positive integer" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="newrelic" %}}
