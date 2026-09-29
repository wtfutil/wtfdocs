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
  pidFilePath: auto
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
        {% with name="pidFilePath",
        desc="<em>Optional</em>. Path to dockerd's pid file, checked before querying the Docker API so a stopped socket-activated daemon isn't started on every refresh.
        The API is only queried when the pid file shows the daemon is running.
        If the file is missing, the daemon is shown as not running.",
        value="<code>auto</code> (checks default location next to the Docker socket), a file path, or unset to disable (default behaviour)" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="docker" %}
{% include "src_path.md" %}
