---
title: "Hacker News"
date: 2018-08-02T16:36:08-04:00
draft: false
weight: 123
---

Displays stories from Hacker News.

## Configuration

```yaml
hackernews:
  enabled: true
  numberOfStories: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  storyType: top
  refreshInterval: 900
```

## Screenshots

<img class="screenshot" src="/imgs/modules/hackernews.png" width="320" height="76" alt="hackernews screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="numberOfStories" desc="_Optional_ Defines number of stories to be displayed. Default: 10." value="Any positive integer" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="storyType" desc="_Optional_ Defines type of stories to be displayed. Default: top." value="`new`, `top`, `job`, `ask`" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected story in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/c desc="Open the selected story's comments in the browser" >}}
  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/o desc="Open the selected story in the browser" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="hackernews" %}}