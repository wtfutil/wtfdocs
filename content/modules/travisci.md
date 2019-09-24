---
title: "TravisCI"
date: 2018-07-18T14:36:08-04:00
draft: false
weight: 240
---

<img class="screenshot" src="/imgs/modules/travisci.png" width="640" height="187" alt="travisci screenshot" />

Displays build information for your Travis CI account.

## Configuration

This module pulls information from api.travis-ci.com (when pro: true) or api.travis-ci.org (when pro: false)

```yaml
travisci:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  compact: true
  limit: 8
  sort_by: "id:desc"
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  pro: false
  refreshInterval: 900
```

{{% attributes %}}
  {{< attributes/apikey name="TravisCI" link="https://developer.travis-ci.org/authentication" envvar="WTF_TRAVIS_API_TOKEN" >}}
  {{< attributes/custom name="baseURL" desc="_Optional_ Your TravisCI Enterprise API URL." value="A valid URL. Can also be set via the `WTF_TRAVIS_BASE_URL` environment variable." >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="compact" desc="When true, displays one line per build entry. When false, displays two lines per entry. Default: false." value="true, false" >}}
  {{< attributes/custom name="sort_by" desc="Sortable by: id, created_at, started_at, finished_at, number, append :desc to any attribute to reverse order. The default value is id:desc. See https://developer.travis-ci.com/resource/builds for more information." >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/custom name="pro" desc="Determines whether or not this module will use the Pro version of Travis CI." value="true, false" >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected build in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}

{{% /keyboard %}}

{{% sourcePath module="travisci" %}}
