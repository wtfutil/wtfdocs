---
title: "GitLab"
date: 2018-06-08T13:14:11-07:00
draft: false
weight: 100
---

Displays information about your projects hosted on GitLab:

#### Open Approval Requests

All open merge requests that are requesting your approval.

#### Open Merge Requests

All open merge requests created by you.

## Configuration

```yaml
gitlab:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 2
    left: 3
    height: 2
    width: 2
  refreshInterval: 300
  projects:
    - "gitlab-org/release/tasks"
    - "gitlab-org/gitlab-ce"
  username: "wtfutil"
```

## Screenshots 

<img class="screenshot" src="/imgs/modules/gitlab.png" width="640" height="390" alt="gitlab screenshot" />

{{% attributes %}}
  {{< attributes/apikey name="GitLab" link="https://docs.gitlab.com/ce/user/profile/personal_access_tokens.html" envvar="WTF_GITLAB_TOKEN" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="domain" desc="_Optional_. Your GitLab corporate domain." value="A valid URI." >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/custom name="projects" desc="A list of GitLab project paths to fetch data for." value="" >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/username name="GitLab" desc="Used to figure out which requests require your approval." >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous git repository" >}}
  {{< keyboard/l desc="Show the next git repository" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous git repository" >}}
  {{< keyboard/arrowFore desc="Show the next git repository" >}}
{{% /keyboard %}}

{{% sourcePath module="gitlab" %}}