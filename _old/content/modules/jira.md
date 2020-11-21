---
title: "Jira"
date: 2018-05-10T10:44:35-07:00
draft: false
weight: 140
---

Displays all Jira issues assigned to you for the specified project.

## Configuration

### Single Jira Project

{{< code lang="yaml" >}}
jira:
  apiKey: "p0d13*********************************************c3"
  colors:
    rows:
      even: "lightblue"
      odd: "white"
  domain: "https://umbrellacorp.atlassian.net"
  email: "chriscummer@me.com"
  enabled: true
  jql: "issueType = Story"
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  project: "ProjectA"
  refreshInterval: 900
  username: "chris.cummer"
  verifyServerCertificate: true
{{< /code >}}

### Multiple Jira Projects

If you want to monitor multiple Jira projects, use the following
configuration (note the difference in `project`):

{{< code lang="yaml" >}}
jira:
  apiKey: "p0d13*********************************************c3"
  colors:
    rows:
      even: "lightblue"
      odd: "white"
  domain: "https://umbrellacorp.atlassian.net"
  email: "chriscummer@me.com"
  enabled: true
  jql: "issueType = Story"
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  project: ["ProjectA", "ProjectB"]
  refreshInterval: 900
  username: "chris.cummer"
  verifyServerCertificate: true
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/jira.png" width="320" height="94" alt="jira screenshot" />

{{% attributes %}}
  {{< attributes/apikey name="Jira" link="https://confluence.atlassian.com/cloud/api-tokens-938839638.html" envvar="WTF_JIRA_API_KEY" >}}
  {{< attributes/border >}}
  {{< attributes/colors/rows >}}
  {{< attributes/custom name="domain" desc="Your Jira corporate domain." value="A valid URI." >}}
  {{< attributes/email name="Jira" >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}

  <tr>
    <td>`jql`</td>
    <td>_Optional_ Custom JQL to be appended to the search query.</td>
    <td>See <a href="https://confluence.atlassian.com/jiracore/blog/2015/07/search-jira-like-a-boss-with-jql">Search Jira like a boss with JQL</a> for details.</td>
  </tr>

  {{< attributes/position >}}
  {{< attributes/custom name="project" desc="The Jira project to fetch information for." >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/username name="Jira" >}}
  {{< attributes/verifyServerCert >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the selected issue in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/j >}}
  {{< keyboard/k >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowDown >}}
  {{< keyboard/arrowUp >}}
{{% /keyboard %}}

{{% sourcePath module="jira" %}}