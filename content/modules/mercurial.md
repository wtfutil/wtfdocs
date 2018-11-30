---
title: "Mercurial"
date: 2018-05-09T14:20:48-07:00
draft: false
weight: 155
---

<img class="screenshot" src="/imgs/modules/mercurial.png" width="710" height="248" alt="mercurial screenshot" />

Displays information about local mercurial repositories: branch, changed
files, and recent commits.

#### Branch

The name of the currently-active mercurial branch.

#### Changed Files

A list of all the files that have changed since the last
commit, and their status.

#### Recent Commits

A list of `n` recent commits, who committed it, and when.

## Source Code

```bash
wtf/mercurial/
```

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Show the previous mercurial repository.

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Show the next mercurial repository.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Show the previous mercurial repository.

<span class="caption">Key:</span> `→` <br />
<span class="caption">Action:</span> Show the next mercurial repository.

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

### Attributes

`commitCount` <br />
The number of past commits to display. <br />
Values: A positive integer, `0..n`.

`commitFormat` <br />
_Optional_ The string format for the commit message. <br />

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`focusChar` <br />
Define one of the number keys as a short cut key to access the widget. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

`repositories` <br />
Defines which mercurial repositories to watch. <br />
Values: A list of zero or more local file paths pointing to valid mercurial repositories.
