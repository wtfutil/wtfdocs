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
    - "wtfutil/wtf"
    - "wtfutil/docs"
    - "umbrella-corp/wesker-api"
  uploadURL: ""
  username: "wtfutil"
```

{{% attributes %}}
  {{< attributes/apikey name="GitHub" link="https://blog.github.com/2013-05-16-personal-api-tokens/" >}}

  <tr>
    <td>`baseURL`</td>
    <td>_Optional_ Your <a href="https://developer.github.com/enterprise/2.13/v3/enterprise-admin/">GitHub Enterprise</a> API URL.</td>
  </tr>

  {{< attributes/border >}}
  {{< attributes/custom name="customQueries" desc="Filters for pull requests and issues." value="" >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="enableStatus" desc="Whether or not to display pull request mergeability status (`dirty`, `clean`, `unstable`, `blocked`)." value="true, false" >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="repositories" desc="A list of github repos to fetch data for." value="" >}}

  <tr>
    <td>`uploadURL`</td>
    <td>_Optional_ Your <a href="https://developer.github.com/enterprise/2.13/v3/enterprise-admin/">GitHub Enterprise</a> upload URL (often the same as the API URL).</td>
    <td></td>
  </tr>

  {{< attributes/username name="GitHub" desc="Used to figure out which review requests you've been added to." >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected repository in a browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous git repository" >}}
  {{< keyboard/l desc="Show the next git repository" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous git repository" >}}
  {{< keyboard/arrowFore desc="Show the next git repository" >}}
{{% /keyboard %}}

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
