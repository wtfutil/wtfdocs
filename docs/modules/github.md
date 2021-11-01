![github](/assets/services/github.png){: align=left width=128 height=128}

# GitHub

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
  refreshInterval: 5m
  repositories:
    - "wtfutil/wtf"
    - "wtfutil/docs"
    - "umbrella-corp/wesker-api"
  uploadURL: ""
  username: "wtfutil"
```

## Screenshots

<img class="screenshot" src="/assets/modules/github.png" width="480" height="288" alt="github screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="GitHub", envvar="WTF_GITHUB_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}
    
        {% with name="baseURL", desc="<code>Optional</code> Your GitHub Enterprise API URL.", value="Your API URL. Leave it empty to use the <code>WTF_GITHUB_BASE_URL</code> environment variable." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

       {% with name="customQueries", desc="Filters for pull requests and issues.", value="See below for examples." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="enableStatus", desc="Whether or not to display pull request mergeability status (<code>dirty</code>, <code>clean</code>, <code>unstable</code>, <code>blocked</code>).", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="repositories", desc="A list of github repos to fetch data for." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showMyPullRequests", desc="<code>Optional</code> Whether or not to display the 'My Pull Requests' section. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showOpenReviewRequests", desc="<code>Optional_</code> Whether or not to display the 'Open Review Requests' section. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showStats", desc="<code>Optional</code> Whether or not to display the 'Stats' section. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="uploadURL", desc="<code>Optional</code> Your GitHub Enterprise upload URL (often the same as the API URL).", value="Your API URL. Leave it empty to use the <code>WTF_GITHUB_UPLOAD_URL</code> environment variable." %}
            {% include "attributes/custom.md" %}
        {% endwith %}


        {% set service="GitHub" %}
        {% set undesc="Used to figure out which review requests you've been added to." %}
        {% include "attributes/username.md" %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected Pull Request or Issue in the browser" %}
    {% include "keyboard/return.md" %}

    {% set insert="Open the selected repository in the browser" %}
    {% include "keyboard/insert.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Show the previous git repository" %}
    {% include "keyboard/h.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set l="Show the next git repository" %}
    {% include "keyboard/l.md" %}

    {% set p="Open the selected Pull Request in the browser" %}
    {% include "keyboard/p.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous git repository" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next git repository" %}
    {% include "keyboard/arrowFore.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

## Custom Query Examples

Custom queries allow you to filter pull requests and issues however you like. Give the query a 
title and a filter. Filters can be copied directly from GitHub's UI.

```yaml
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

{% set src="github" %}
{% include "src_path.md" %}