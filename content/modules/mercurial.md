---
title: "Mercurial"
date: 2018-05-09T14:20:48-07:00
draft: false
weight: 155
---

Displays information about local mercurial repositories: branch, changed
files, and recent commits.

#### Branch

The name of the currently-active mercurial branch.

#### Changed Files

A list of all the files that have changed since the last
commit, and their status.

#### Recent Commits

A list of `n` recent commits, who committed it, and when.

## Configuration

```yaml
mercurial:
  commitCount: 5
  commitFormat: "[forestgreen]{rev}:{phase} [white]{desc|firstline|strip} [grey]{author|person} {date|age}[white]"
  enabled: true
  position:
    top: 0
    left: 3
    height: 2
    width: 2
  refreshInterval: 8
  repositories:
  - "/Users/user/fakelib"
  - "/Users/user/fakeapp"
```

## Screenshots

<img class="screenshot" src="/imgs/modules/mercurial.png" width="710" height="248" alt="mercurial screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/custom name="commitCount" desc="The number of past commits to display." value="Any positive integer" >}}
  {{< attributes/custom name="commitFormat" desc="_Optional_ The string format for the commit message." value="" >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="repositories" desc="A list of Mercurial repositories to watch." value="A list of zero or more local file paths pointing to valid mercurial repositories." >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous Mercurial repository" >}}
  {{< keyboard/l desc="Show the next Mercurial repository" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous Mercurial repository" >}}
  {{< keyboard/arrowFore desc="Show the next Mercurial repository" >}}
{{% /keyboard %}}

{{% sourcePath module="mercurial" %}}