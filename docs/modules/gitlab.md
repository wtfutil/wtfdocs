# GitLab

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
  projects:
    - "gitlab-org/gitlab-ce"
    - "gitlab-org/release/tasks"
  refreshInterval: 5m
  username: "wtfutil"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="GitLab", envvar="WTF_GITLAB_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="domain", desc="<code>Optional</code> Your GitLab corporate domain.", value="A valid URI." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="projects", desc="A list of GitLab project paths to fetch data for." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="GitLab" %}
        {% set undesc="Used to figure out which requests require your approval." %}
        {% include "attributes/username.md" %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Show the previous GitLab repository" %}
    {% include "keyboard/h.md" %}

    {% set l="Show the next GitLab repository" %}
    {% include "keyboard/l.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous GitLab repository" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next GitLab repository" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="gitlab" %}
{% include "src_path.md" %}