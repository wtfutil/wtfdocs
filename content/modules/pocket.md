---
title: 'Pocket'
date: 2020-05-01T18:55:37-08:00
draft: false
---

Displays Pocket Saved Articles.

## Configuration

```yaml
pocket:
    enabled: true
    position:
        top: 0
        left: 3
        height: 4
        width: 2
    consumerKey: '88*******************'
    refreshInterval: 1
```

{{% attributes %}}
{{< attributes/custom name="consumer_key" desc="The consumer key of pocket app obtained from https://getpocket.com/developer/apps/new, make sure to have add, modify and retrieve permissions" value="888**************************" >}}
{{< attributes/border >}}
{{< attributes/enabled >}}
{{< attributes/focusChar >}}
{{< attributes/position >}}
{{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% keyboard %}}
{{< keyboard/foreSlash >}}
{{< keyboard/return desc="Open the article in the browser" >}}

{{< keyboard/spacer >}}

{{< keyboard/j >}}
{{< keyboard/k >}}

{{< keyboard/spacer >}}

{{< keyboard/a desc="Toggle link archive/unarchive">}}
{{< keyboard/t desc="Toggle view archived links/active links">}}

{{< keyboard/spacer >}}

{{< keyboard/arrowDown >}}
{{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="pocket" %}}
