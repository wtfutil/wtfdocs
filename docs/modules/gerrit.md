# Gerrit

Displays information about your projects hosted on Gerrit:

#### Open Incoming Reviews

All open reviews that are requesting your approval.

#### My Outgoing Reviews

All open reviews created by you.

## Configuration

```yaml
gerrit:
  colors:
    rows:
      even: "lightblue"
      odd: "white"
  domain: https://gerrit-review.googlesource.com
  enabled: true
  password: "mypassword"
  position:
    top: 2
    left: 3
    height: 2
    width: 2
  projects:
  - org/test-project"
  - dotfiles
  refreshInterval: 5m
  username: "myname"
  verifyServerCertificate: false
```

## Screenshots

<img class="screenshot" src="/assets/modules/gerrit.png" width="640" height="167" alt="gerrit screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="domain", desc="Your Gerrit corporate domain." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Gerrit" %}
        {% set pwdesc="Leave this empty to use the <code>WTF_GERRIT_PASSWORD</code> environment variable." %}
        {% include "attributes/password.md" %}

        {% with name="projects", desc="A list of Gerrit project names to fetch data for." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Gerrit" %}
        {% include "attributes/username.md" %}

        {% include "attributes/verifyServerCert.md" %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the selected review in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Show the previous project" %}
    {% include "keyboard/h.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set l="Show the next project" %}
    {% include "keyboard/l.md" %}

    {% set o="Open the selected review in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous project" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next project" %}
    {% include "keyboard/arrowFore.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="gerrit" %}
{% include "src_path.md" %}