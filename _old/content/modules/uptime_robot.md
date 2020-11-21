---
title: "UptimeRobot"
date: 2020-10-14T09:14:41-08:00
draft: false
weight: 260
---

Connect to the [UptimeRobot](https://uptimerobot.com) API.

## Configuration

{{< code lang="yaml" >}}
uptimerobot:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  offlineFirst: true
  position:
    top: 0
    left: 1
    height: 2
    width: 1
  refreshInterval: 3600
  uptimePeriods: 7-30
{{< /code >}}

{{% attributes %}}
  {{< attributes/apikey name="UptimeRobot" link="https://uptimerobot.com/api/" envvar="WTF_UPTIMEROBOT_APIKEY" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="offlineFirst" desc="_Optional_ Display offline monitors at the top." value="`true`, `false`" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="uptimePeriods" desc="_Optional_ The periods over which to display uptime (in days, dash-separated)." value="" >}}
{{% /attributes %}}

{{% sourcePath module="uptimerobot" %}}