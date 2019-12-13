---
title: "Logger"
date: 2018-06-16T14:22:18-07:00
draft: false
weight: 150
---

Displays the contents of the WTF log file. The log file is located at `~/.config/wtf/log.txt`.

## Usage

To log to this file in your own modules:

```golang
require "github.com/wtfutil/wtf/logger"
logger.Log("This is a log entry")
```

## Configuration

```yaml
logger:
  enabled: true
  position:
    top: 5
    left: 4
    height: 2
    width: 1
  refreshInterval: 1
```

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

## Keyboard Controls

Arrow keys scroll through the log file.

{{% sourcePath module="logger" %}}