---
title: "Status Pages"
date: 2018-05-09T14:20:48-07:00
draft: false
hidden: true
weight: 80
---

Various services provide status apis which are accessible. For example, the
slack status api at `https://status.slack.com/api/v2.0.0/current`

This can be accomplished with [jq](https://stedolan.github.io/jq/) and the
cmdrunner module.

First, create a shell script:

```shell
#!/bin/sh

curl -s https://status.slack.com/api/v2.0.0/current | \
  jq -r '"Status: " + (if (.status == "active") then "Active Incident" else "Ok" end),"Last Updated: " + .date_updated,if (.active_incidents[] | length) > 0 then "Active Incidents\n" + .active_incidents[] .title else "" end'
```

Second, the following wtfutil config:

```yaml
slack_status:
  cmd: "slack_status_check.sh"
  enabled: true
  type: "cmdrunner"
  title: "Slack Status"
  position:
    top: 5
    left: 0
    height: 3
    width: 4
  refreshInterval: 30
```

<img class="screenshot" src="/imgs/modules/cmdrunner/slackstatus.png" alt="status screenshot" />
