# Jenkins

Displays Jenkins status of given builds in a project or view.

## Configuration

```yaml
jenkins:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 2
    left: 3
    height: 2
    width: 3
  refreshInterval: 300
  successBallColor: "green"
  jobNameRegex: ^[a-z]+\[[0-9]+\]$
  url: "https://jenkins.domain.com/jenkins/view_url"
  user: "username"
  verifyServerCertificate: true
```

## Screenshots

<img class="screenshot" src="/assets/modules/jenkins.png" alt="jenkins screenshot" width="320" height="68" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Jenkins", envvar="WTF_JENKINS_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="jobNameRegex", desc="<code>Optional</code> A regex that filters the jobs shown in the widget. Any jobs matching the regular expression will be shown.", value="A valid regex, e.g. <code>^[a-z]+\[[0-9]+\]$</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="successBallColor", desc="Changes the default color of successful Jenkins jobs to the color of your choosing.", value="Any valid color name, <code>blue</code>, <code>green</code>, <code>purple</code>, <code>yellow</code>, etc." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="url", desc="The URL to your Jenkins project or view.", value="A valid URI." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Jenkins" %}
        {% include "attributes/username.md" %}

        {% include "attributes/verifyServerCert.md" %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected job in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}
    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="jenkins" %}
{% include "src_path.md" %}