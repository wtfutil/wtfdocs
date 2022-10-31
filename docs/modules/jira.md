# Jira

Displays all Jira issues assigned to you for the specified project.

## Configuration

### Single Jira Project

```yaml
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
  refreshInterval: 15m
  username: "chris.cummer"
  verifyServerCertificate: true
```

### Multiple Jira Projects

If you want to monitor multiple Jira projects, use the following
configuration (note the difference in `project`):

```yaml
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
  refreshInterval: 15m
  username: "chris.cummer"
  verifyServerCertificate: true
```

## Screenshots

<img class="screenshot" src="/assets/modules/jira.png" width="320" height="94" alt="jira screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Jira", envvar="WTF_JIRA_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% include "attributes/colors/rows.md" %}

        {% with name="domain", desc="Your Jira corporate domain.", value="A valid URI." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Jira" %}
        {% include "attributes/email.md" %}

        {% with name="jql", desc="<em>Optional</em> Custom JQL to be appended to the search query.", value="See <a href='https://confluence.atlassian.com/jiracore/blog/2015/07/search-jira-like-a-boss-with-jql'>Search Jira Like a Boss with JQL</a> for details." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="project", desc="An array of projects to get data from", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Jira" %}
        {% include "attributes/username.md" %}

        {% include "attributes/verifyServerCert.md" %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

  </tbody>
</table>

{% set src="jira" %}
{% include "src_path.md" %}
