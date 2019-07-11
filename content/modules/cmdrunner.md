---
title: "CmdRunner"
date: 2018-05-17T17:17:10-07:00
draft: false
weight: 40
---

Runs a terminal command on a schedule.

## Configuration

```yaml
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
```

{{% attributes %}}
  {{< attributes/custom name="args" desc="The arguments to the command, with each item as an element in an array." value="" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="cmd" desc="The terminal command to be run, withouth the arguments. Ie: `ping`, `whoami`, `curl`." value="" >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

### Attributes

`args` <br />
The arguments to the command, with each item as an element in an array.
Example: for `curl -I cisco.com`, the arguments array would be `["-I", "cisco.com"]`.

`cmd` <br />
The terminal command to be run, withouth the arguments. Ie: `ping`,
`whoami`, `curl`. <br />

## Examples

 * [iStats](/modules/cmdrunner/istats)
 * [Status Pages](/modules/cmdrunner/statuspages)

{{% sourcePath module="cmdrunner" %}}