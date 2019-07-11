---
title: "Git"
date: 2018-05-09T14:20:48-07:00
draft: false
weight: 80
---

<img class="screenshot" src="/imgs/modules/git.png" width="720" height="292" alt="git screenshot" />

Displays information about local git repositories: branch, changed
files, and recent commits.

#### Branch

The name of the currently-active git branch.

#### Changed Files

A list of all the files that have changed since the last
commit, and their status.

#### Recent Commits

A list of `n` recent commits, who committed it, and when.

## Configuration

```yaml
git:
  commitCount: 5
  commitFormat: "[forestgreen]%h [grey]%cd [white]%s [grey]%an[white]"
  dateFormat: "%H:%M %d %b %y"
  enabled: true
  position:
    top: 0
    left: 3
    height: 2
    width: 2
  refreshInterval: 8
  repositories:
  - "/Users/chris/go/src/github.com/wtfutil/wtf"
  - "/Users/user/fakeapp"
```

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/custom name="commitCount" desc="The number of past commits to display." value="Any positive integer" >}}
  {{< attributes/custom name="commitFormat" desc="_Optional_ The string format for the commit message." value="" >}}
  {{< attributes/dateFormat >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="repositories" desc="A list of git repositories to watch." value="Zero or more local file paths pointing to valid git repositories." >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/c desc="Check out branch" >}}
  {{< keyboard/h desc="Show the previous git repository" >}}
  {{< keyboard/l desc="Show the next git repository" >}}
  {{< keyboard/p desc="Pull repo" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous git repository" >}}
  {{< keyboard/arrowFore desc="Show the next git repository" >}}
{{% /keyboard %}}

{{% sourcePath module="git" %}}
