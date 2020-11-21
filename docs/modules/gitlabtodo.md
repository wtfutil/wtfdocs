# GitLab Todo

View your GitLab Todos.

## Configuration

```yaml
gitlabtodo:
    apiKey: "dexxxxxxxxxxxxxxxxxxxxxxxxxx34"
    domain: "example.com"
    enabled: true
    numberOfTodos: 12,
    position:
        top: 2
        left: 3
        height: 2
        width: 2
    refreshInterval: 300
    showProject: true
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
{% with name="GitLab", envvar="WTF_GITLAB_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

{% with name="domain", desc="Your GitLab corporate domain.", value="" %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="numberOfTodos", desc="<em>Optional</em> Defines number of stories to be displayed. Default is <code>10</code>.", value="" %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="showProject", desc="<em>Optional</em> Determines whether or not to show the project a given todo is for. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>." %}
{% include "attributes/custom.md" %}
{% endwith %}
    </tbody>
</table>

{% set src="gitlabtodo" %}
{% include "src_path.md" %}