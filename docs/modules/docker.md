<img src="/assets/services/docker.png" width="128" height="97" alt="docker" title="docker" style="float: left; padding-right: 8px;" />

# Docker

Displays information about currently-running Docker processes.

## Configuration

```yaml
docker:
  type: docker
  enabled: true
  labelColor: lightblue
  position:
    top: 0
    left: 0
    height: 3
    width: 3
  refreshInterval: 1s
```

## Screenshots

<img class="screenshot" src="/assets/modules/docker.png" width="275" height="320" alt="docker screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>labelColor</code>
        <br />
        The color to display the row labels in.
    </td>
    <td></td>
</tr>
    </tbody>
</table>

{% set src="docker" %}
{% include "src_path.md" %}