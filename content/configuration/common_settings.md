---
title: "Common Settings"
date: 2019-09-22T18:20:35-07:00
draft: false
weight: 7
---

The following settings are common to all modules. Common settings have logical defaults and are all optional. An explicitly-defined common setting will over-ride a module's internal default setting value.

An example with all common settings explicitly configured.

{{< code lang="yaml" >}}
feedreader:
  enabled: true
  feeds:
  - https://news.ycombinator.com/rss
  feedLimit: 10
  focusable: false
  position:
    top: 2
    left: 2
    width: 1
    height: 1
  title: "Hacker News"
  updateInterval: 14400
{{< /code >}}

{{% attributes %}}
  {{< attributes/enabled >}}
  {{< attributes/focusable >}}
  {{< attributes/title >}}
{{% /attributes %}}