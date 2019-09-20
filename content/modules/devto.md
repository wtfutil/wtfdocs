---
title: "DEV (dev.to)"
date: 2018-08-02T16:36:08-04:00
draft: false
weight: 60
---

<img class="screenshot" src="/imgs/modules/devto.png" width="100" height="100" alt="dev.to logo"/>

Displays stories from The Practical DEV [dev.to](https://dev.to).

## Configuration

```yaml
devto:
  enabled: true
  numberOfArticles: 10
  position:
    top: 1
    left: 1
    height: 1
    width: 2
  contentTag: "showdev" 
  contentUsername: "victoravelar"
  contentState: "rising"
```
{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="numberOfArticles" desc="_Optional_ Defines number of articles to be displayed. Default: 10." value="Any positive integer < 20" >}}
  {{< attributes/custom name="contentTag" desc="_Optional_ List articles from a specific tag. Default: empty" value="Visit https://dev.to/tags for a list of valid values" >}}
  {{< attributes/custom name="contentUsername" desc="_Optional_ List articles from a specific user. Default: empty" value="Try your favorite username or victoravelar" >}}
  {{< attributes/custom name="contentState" desc="_Optional_ Alters the feed output. Default: empty" value="`rising`, `fresh`, `ben`" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected story in the browser" >}}
  {{< keyboard/esc desc="Cancel selection" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="devto" %}}