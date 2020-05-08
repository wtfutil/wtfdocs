---
title: "Feed Reader"
date: 2019-07-04T05:53:08-04:00
draft: false
weight: 65
---

A rudimentary RSS & Atom feed reader.

## Configuration

{{< code lang="yaml" >}}
feedreader:
  enabled: true
  feeds:
  - https://news.ycombinator.com/rss
  - http://feeds.reuters.com/Reuters/worldNews
  feedLimit: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 14400
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/feedreader.png" width="320" height="94" alt="feedreader screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="feedLimit" desc="The number of stories from each feed to be displayed. Default is `-1`, which will display all available stories." value="Any integer greater than zero. Values zero or less will display all." >}}
  {{< attributes/custom name="feeds" desc="List of RSS or Atom feed URLs." value="" >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected story in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/o desc="Open the selected story in the browser" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="feedreader" %}}