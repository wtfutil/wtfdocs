# Kubernetes

Displays information about a Kubernetes cluster.

## Configuration

```yaml
kubernetes:
  enabled: true
  kubeconfig: "/Users/testuser/.kube/config"
  namespaces:
  - internal
  - public
  - systems
  objects:
  - deployments
  - nodes
  - pods
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 5m
  title: "Build System"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="context", desc="The Kubernetes context to use. If blank, it uses the default context." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="kubeconfig", desc="The absolute path to your Kubernetes config file." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="namespaces", desc="A list of namespaces to monitor. Defaults to all if empty." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="objects", desc="A list of Kubernetes objects to display.", value="Any of <code>nodes</code>, <code>pods</code>, and/or <code>deployments</code>." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="kubernetes" %}
{% include "src_path.md" %}