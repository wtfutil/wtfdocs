---
title: "Subreddit"
date: 2019-09-27T19:48:42+01:00
draft: false
weight: 207
---

Displays stories from a specific subreddit.

## Configuration

{{< code lang="yaml" >}}
subreddit:
  enabled: true
  numberOfPosts: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  sortOrder: top
  subreddit: "news"
  topTimePeriod: month
  refreshInterval: 900
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/subreddit.png" width="320" height="76" alt="subreddit module screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="numberOfPosts" desc="_Optional_ Defines number of stories to be displayed. Default: 10. Note that the module only makes one request, so the maximum is 25." value="Any positive integer equal to or less than 25" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="sortOrder" desc="_Optional_ Defines the order to sort the posts in the subreddit. Default: hot." value="`new`, `top`, `hot`" >}}
  {{< attributes/custom name="subreddit" desc="_Required_ The subreddit to display links from." value="Any subreddit" >}}
  {{< attributes/custom name="topTimePeriod" desc="_Optional_ Defines the time period to choose top posts from. Default: all" value="`hour`, `day`, `week`, `month`, `year`, `all`" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected link in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/c desc="Open the selected link's Reddit comments in the browser" >}}
  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/o desc="Open the selected link in the browser" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="subreddit" %}}