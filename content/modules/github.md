---
title: "GitHub"
date: 2018-05-09T19:20:20-07:00
draft: false
weight: 90
---

<img class="screenshot" src="/imgs/modules/github.png" width="480" height="288" alt="github screenshot" />

Displays information about your git repositories hosted on GitHub:

#### Open Review Requests

All open code review requests assigned to you.

#### Open Pull Requests

All open pull requests created by you.

#### Custom Queries

Create filters to manage PRs and issues however you like.

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Show the previous git repository.

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Show the next git repository.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Show the previous git repository.

<span class="caption">Key:</span> `→` <br />
<span class="caption">Action:</span> Show the next git repository.

<span class="caption">Key:</span> `Return` <br />
<span class="caption">Action:</span> Open the selected repository in a browser.

## Configuration

```yaml
github:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  baseURL: ""
  customQueries:
    othersPRs:
      title: "Others Pull Requests"
      filter: "is:open is:pr -author:wtfutil"
  enabled: true
  enableStatus: true
  position:
    top: 2
    left: 3
    height: 2
    width: 2
  refreshInterval: 300
  repositories:
    wesker-api: "UmbrellaCorp"
    wtf: "wtfutil"
  uploadURL: ""
  username: "wtfutil"
```

### Attributes

`apiKey` <br />
Value: Your <a href="https://blog.github.com/2013-05-16-personal-api-tokens/">GitHub API</a> token.

`baseURL` <br />
_Optional_ <br />
Value: Your <a href="https://developer.github.com/enterprise/2.13/v3/enterprise-admin/">GitHub Enterprise</a> API URL.

`enabled` <br />
Whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`enableStatus` <br />
Display pull request mergeability status ('dirty', 'clean', 'unstable',
'blocked').<br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`focusChar` <br />
Define one of the number keys as a short cut key to access the widget. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

`repositories` <br />
A list of github repos to fetch data for. <br />
Example: `wtfutil/wtf` 

`uploadURL` <br />
_Optional_ <br />
Value: Your <a href="https://developer.github.com/enterprise/2.13/v3/enterprise-admin/">GitHub Enterprise</a> upload URL (often the same as API URL).

`username` <br />
Your GitHub username. Used to figure out which review requests you've
been added to.

## Custom Query Examples

Custom queries allow you to filter pull requests and issues however you like. Give the query a 
title and a filter. Filters can be copied directly from GitHub's UI.

```
customQueries:
  othersPRs:
    # Displays pull requests that are not assigned to you
    title: "Others Pull Requests"
    filter: "is:open is:pr -author:[your github username]"
  openIssues:
    # Displays issues that are assigned to you
    title: "My Issues"
    filter: "is:issue state:open author:[your github username]"
  otherIssues:
    # Displays issues not assigned to you, order by their updated_at date
    perPage: 10
    title: "Others Issues"
    filter: "is:issue state:open -author:[your github username] sort:updated-desc"
```

{{% sourcePath module="github" %}}
