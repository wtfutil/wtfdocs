# Resource Usage

Displays CPU and memory usage.

## Configuration

```yaml
resourceusage:
  cpuCombined: false
  enabled: true
  position:
    top: 1
    left: 1
    height: 1
    width: 1
  refreshInterval: 1
  showCPU: true
  showMem: true
  showSwp: true
```

## Screenshots

<img class="screenshot" src="/assets/modules/resource_usage.png" width="279" height="193" alt="resource usage screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="cpuCombined", desc="<em>Optional</em> Whether or not to display the CPUs as one combined value. Default: <code>false</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="graphIcon", desc="<em>Optional</em> The character to use to display stars in the graph. Default: <code>|</code>.", value="Any visible alphanumeric character." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="graphStars", desc="<em>Optional</em> The maximum number of stars to display in the graph. Default: <code>20</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showCPU", desc="<em>Optional</em> Whether or not to display the CPU usage. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showMem", desc="<em>Optional</em> Whether or not to display the memory usage. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showSwp", desc="<em>Optional</em> Whether or not to display the swap memory usage. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="resourceusage" %}
{% include "src_path.md" %}