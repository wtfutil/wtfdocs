---
title: "Zendesk"
date: 2018-07-23T18:55:37-08:00
draft: false
weight: 280
---

Displays Zendesk tickets.

## Configuration

```yaml
zendesk:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  position:
    top: 0
    left: 2
    height: 1
    width: 1
  status: "new"
  subdomain: "your_domain"
  username: "your_email@acme.com"
```

{{% attributes %}}
  {{< attributes/apikey name="Zendesk" link="" envvar="ZENDESK_API" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="status" desc="The status of tickets you want to retrieve." value="`new`, `open`, `pending`, `hold`" >}}
  {{< attributes/custom name="subdomain" desc="Your Zendesk subdomain." >}}
  {{< attributes/username name="Zendesk" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected ticket in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="zendesk" %}}