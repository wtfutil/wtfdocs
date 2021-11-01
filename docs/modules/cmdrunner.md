# CmdRunner

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
  refreshInterval: 30s
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>args</code>
        <br />
        The arguments to the command, with each item as an element in an array.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>cmd</code>
        <br />
        The terminal command to be run, withouth the arguments. Ie: <code>ping</code>, <code>whoami</code>, <code>curl</code>.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>maxLines</code>
        <br />
        <em>Optional</em> The maximum number of lines to keep in the buffer. Default: <code>256</code>.
    </td>
    <td>Any positive integer.</td>
</tr>
<tr>
    <td>
        <code>pty</code>
        <br />
        <em>Optional</em> Run the command in a pseudo-terminal. Some apps will behave differently if they are run in a terminal. For example, some apps will produce colorized output in a terminal, and non-colorized output otherwise. Default: <code>false</code>.
    </td>
    <td><code>true</code>, <code>false</code></td>
</tr>
<tr>
    <td>
        <code>tail</code>
        <br />
        <em>Optional</em> Automatically scroll with new output. Default: <code>false</code>.
    </td>
    <td><code>true</code>, <code>false</code></td>
</tr>
    </tbody>
</table>

## Known limitations

Internally, CmdRunner relies on Golang's `exec.Command()` to run terminal commands. As it does not invoke the system shell, not all commands are supported. To quote [Golang docs](https://pkg.go.dev/os/exec), it "does not expand any glob patterns or handle other expansions, pipelines, or redirections typically done by shells." 

## Examples

### `brew outdated`

Displays a list of all the installed [Homebrew](https://brew.sh) recipes that have an update available for them.

```yaml
brew_outdated:
  args: ["outdated"]
  cmd: "brew"
  enabled: true
  position:
    top: 3
    left: 1
    width: 2
    height: 1
  type: cmdrunner
```

### iStats

[iStats](https://github.com/Chris911/iStats) is a command line tool to view system stats on OSX.

```yaml
istats:
  args: ["all"]
  cmd: "istats"
  enabled: true
  type: "cmdrunner"
  position:
    top: 0
    left: 3
    height: 2
    width: 2
  refreshInterval: 1s
```

### Status Pages

Various services provide status apis which are accessible. For example, the
slack status api at `https://status.slack.com/api/v2.0.0/current`

This can be accomplished with [jq](https://stedolan.github.io/jq/) and the
cmdrunner module.

First, create a shell script:

```bash
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
  refreshInterval: 30s
```

### wego

[wego](https://github.com/schachmat/wego) is a command line tool to view weather, from a variety of weather services

```yaml
weather:
  args: ["0"]
  cmd: "wego"
  enabled: true
  type: "cmdrunner"
  position:
    top: 0
    left: 0
    height: 1
    width: 2
  refreshInterval: 100s
```

{% set src="cmdrunner" %}
{% include "src_path.md" %}
