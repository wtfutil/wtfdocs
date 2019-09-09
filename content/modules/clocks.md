---
title: "Clocks"
date: 2018-05-07T19:47:31-07:00
draft: false
weight: 30
---

<img src="/imgs/modules/clocks.png" class="screenshot" width="320" height="191" alt="clocks screenshot" />

Displays a configurable list of world clocks, the local time, and date.

## Configuration

```yaml
clocks:
  colors:
    rows:
      even: "lightblue"
      odd: "white"
  enabled: true
  locations:
    # From https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
    Avignon: "Europe/Paris"
    Barcelona: "Europe/Madrid"
    Dubai: "Asia/Dubai"
    New York: "America/New York"
    Toronto: "America/Toronto"
    UTC: "Etc/UTC"
    Vancouver: "America/Vancouver"
  position:
    top: 4
    left: 0
    height: 1
    width: 1
  refreshInterval: 15
  # Valid options are: alphabetical, chronological
  sort: "alphabetical"
```

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/rows >}}
  {{< attributes/dateFormat >}}
  {{< attributes/enabled >}}

  <tr><td>`locations`</td><td>A list of timezone for the clocks to be displayed.</td><td>Any <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">TZ database timezone.</td></tr>

  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

  {{< attributes/custom name="sort" desc="The order in which to sort the clocks." value="`alphabetical` or `chronological`. `alphabetical` will sort in acending order by `key`, `chronological` will sort in ascending order by date/time." >}}
  
  {{< attributes/timeFormat >}}
{{% /attributes %}}

{{% sourcePath module="clocks" %}}
