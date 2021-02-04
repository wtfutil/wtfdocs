# Asana

Displays Asana Tasks filtered by Workspace, Project or even by Sections within a Project.

The `apiKey` is a Personal Access Token and can be generated [here](https://app.asana.com/0/developer-console)

The module includes keyboard navigation too, so you can select a task with `j` and `k`, and `o`pen it. For more keyboard navigation options press `?`.

## Configuration

```yaml
asana:
  enabled: true
  apiKey: "*******"
  mode: "project_sections"
  projectId: 123456789
  workspaceId: 123456789
  allUsers: false
  hideComplete: false
  sections:
    - "Doing"
    - "Backlog"
    - "Complete"
  updateInterval: 300
  position:
    top: 0
    left: 0
    width: 1
    height: 3
```

## Screenshots

<img class="screenshot" src="/assets/modules/asana.png" width="666" height="782" alt="asana screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Asana", envvar="WTF_ASANA_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        <tr>
            <td>
                <code>mode</code>
                <br />
                What mode to query Asana. There are three modes:<br />
                <ul><li><code>project</code> - Will fetch all Asana Tasks in the project specified in the <code>projectId</code> attribute</li>
                <li><code>project_sections</code> - Will fetch all Asana Tasks in the project specified, under the supplied <code>sections</code>.</li>
                <li><code>workspace</code> - Will fetch all of the tasks in the workspace, assigned to you. You must specify a <code>workspaceId</code></li></ul>
            </td>
            <td><code>project</code>, <code>project_sections</code>, or <code>workspace</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>projectId</code>
                <br />
                <em>Optional</em> The Asana Project to fetch tasks from. Only applicable if you specify the <code>project</code> or <code>project_sections</code> <code>mode</code>
            </td>
            <td>A valid Asana Project Identifier integer
            </td>
        </tr>
        <tr>
            <td>
                <code>workspaceId</code>
                <br />
                <em>Optional</em> The Asana Workspace to fetch tasks from. This will only return tasks assigned to you. Only applicable if you specify the <code>workspace</code> <code>mode</code>
            </td>
            <td>A valid Asana Workspace Identifier integer
            </td>
        </tr>
        <tr>
            <td>
                <code>allUsers</code>
                <br />
                <em>Optional</em> When querying for <code>project</code> or <code>project_sections</code> you can optionally display tasks that are assigned to other users. Defaults to <code>false</code>.
            </td>
            <td><code>true</code> or <code>false</code></td>
        </tr>
        <tr>
            <td>
                <code>hideComplete</code>
                <br />
                <em>Optional</em> When querying for tasks you can optionally hide tasks that have been marked as complete. Defaults to <code>false</code>.
            </td>
            <td><code>true</code> or <code>false</code></td>
        </tr>
        <tr>
            <td>
                <code>sections</code>
                <br />
                <em>Optional</em> When the <code>mode</code> is <code>project_sections</code> you can list the sections you want to fetch the tasks from
            </td>
            <td>A list of valid Section names</td>
        </tr>
    </tbody>
</table>

{% set src="asana" %}
{% include "src_path.md" %}
