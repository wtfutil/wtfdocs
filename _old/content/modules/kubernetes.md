---
title: "Kubernetes"
date: 2019-08-19T14:33:21-07:00
draft: false
weight: 145
---

Displays information about a Kubernetes cluster.

## Configuration

{{< code lang="yaml" >}}
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
  refreshInterval: 300
  title: "Build System"
{{< /code >}}

{{% attributes %}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="context" desc="The Kubernetes context to use. If blank, it uses default context." value="" >}}
  {{< attributes/custom name="kubeconfig" desc="The absolute path to your Kubernetes config file." value="" >}}
  {{< attributes/custom name="namespaces" desc="A list of namespaces to monitor. Defaults to all if empty." value="" >}}
  {{< attributes/custom name="objects" desc="A list of Kubernetes objects to display." value="Any of `nodes`, `pods`, and/or `deployments`." >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/title >}}
{{% /attributes %}}

{{% sourcePath module="kubernetes" %}}