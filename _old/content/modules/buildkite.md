---
title: "Buildkite"
date: 2019-10-10T11:07:37-07:00
draft: false
weight: 15
---

Connects to the [Buildkite](https://buildkite.com) REST API and displays status of branches for configured Pipelines.

The API token must have the `read_builds` permission.

## Configuration

{{< code lang="yaml" >}}
buildkite:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  organizationSlug: "acme-corp"
  refreshInterval: 60
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
{{< /code >}}

{{% attributes %}}
  {{< attributes/apikey name="Buildkite" link="https://buildkite.com/docs/apis/rest-api#authentication" envvar="WTF_BUILDKITE_TOKEN" >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="organizationSlug" desc="The slug of your organization" value="`org.slug`" >}}
  {{< attributes/custom name="pipelines" desc="A hash with `pipeline.slug` as keys, mapping to a list of branches" value="" >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

{{% sourcePath module="buildkite" %}}
