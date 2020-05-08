---
title: "CmdRunner"
date: 2018-05-17T17:17:10-07:00
draft: false
weight: 40
---

Runs a terminal command on a schedule.

## Configuration

{{< code lang="yaml" >}}
cmdrunner:
  args: ["-g", "batt"]
  cmd: "pmset"
  enabled: true
  position:
    top: 6
    left: 1
    height: 1
    width: 3
  refreshInterval: 30
{{< /code >}}

{{% attributes %}}
  {{< attributes/custom name="args" desc="The arguments to the command, with each item as an element in an array." value="" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="cmd" desc="The terminal command to be run, withouth the arguments. Ie: `ping`, `whoami`, `curl`." value="" >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="maxLines" desc="The maximum number of lines to keep in the buffer. Default: `256`." value="Any positive integer" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="tail" desc="Automatically scroll with new output. Default: `false`." value="true, false" >}}
  {{< attributes/title >}}
{{% /attributes %}}

## Examples

* [brew outdated](/modules/cmdrunner/brew_outdated)
* [iStats](/modules/cmdrunner/istats)
* [Status Pages](/modules/cmdrunner/statuspages)
* [wego](/modules/cmdrunner/wego)

{{% sourcePath module="cmdrunner" %}}