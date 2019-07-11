---
title: "CircleCI"
date: 2018-06-10T19:26:08-04:00
draft: false
weight: 20
---

<img src="/imgs/modules/circleci.png" class="screenshot" width="609" height="150" alt="circleci screenshot" />

Added in `v0.0.7`.

Displays build information for your CircleCI account.


## Configuration

```yaml
circleci:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 900
```

{{% attributes %}}
  {{< attributes/apikey name="CircleCI" link="https://circleci.com/account/api" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="circleci" %}}