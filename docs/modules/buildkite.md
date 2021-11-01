# Buildkite

Connects to the [Buildkite](https://buildkite.com) REST API and displays status of branches for configured Pipelines.

The API token must have the `read_builds` permission.

## Configuration

```yaml
buildkite:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  organizationSlug: "acme-corp"
  refreshInterval: 1m
  position:
    top: 1
    left: 1
    height: 1
    width: 1
  pipelines:
    pipeline-slug-1:
      branches:
        - "master"
        - "stage"
    pipeline-slug-2:
      branches:
        - "master"
        - "production"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Buildkite", envvar="WTF_BUILDKITE_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        <tr>
            <td>
                <code>organizationSlug</code>
                <br />
                The slug of your organization
            </td>
            <td><code>org.slug</code></td>
        </tr>
        <tr>
            <td>
                <code>pipelines</code>
                <br />
                A hash with <code>pipeline.slug</code> as keys, mapping to a list of branches.
            </td>
            <td></td>
        </tr>

    </tbody>
</table>

{% set src="buildkite" %}
{% include "src_path.md" %}