---
title: "Hacker News"
date: 2018-08-02T16:36:08-04:00
draft: false
weight: 123
---

<img class="screenshot" src="/imgs/modules/hackernews.png" width="320" height="76" alt="hackernews screenshot" />

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
{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/custom name="numberOfStories" desc="_Optional_ Defines number of stories to be displayed. Default: 10." value="Any positive integer" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="storyType" desc="_Optional_ Defines type of stories to be displayed. Default: top." value="`new`, `top`, `job`, `ask`" >}}
{{% /attributes %}}

## Keyboard Commands

<span class="caption">Key:</span> `[return]` <br />
<span class="caption">Action:</span> Open the selected story in the browser.

<span class="caption">Key:</span> `c` <br />
<span class="caption">Action:</span> Open the selected story's comments in the browser.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next story in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous story in the list.

<span class="caption">Key:</span> `o` <br />
<span class="caption">Action:</span> Open the selected story in the browser.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Refresh the data.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next story in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous story in the list.


{{% sourcePath module="hackernews" %}}