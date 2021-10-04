# Healthchecks

Connect to the [Healthchecks](https://healthchecks.io) API.

## Configuration

```yaml
healthchecks:
  type: healthchecks
  enabled: true
  apiKey: "XXXX"
  apiURL: "https://healthchecks.io/"
  tags:
    - backup
  position:
    top: 0
    left: 1
    height: 2
    width: 1
```

## Screenshots

<img class="screenshot" src="/assets/modules/healthchecks.png" width="688" height="420" alt="Healthchecks screenshot" />


## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="Healthchecks", envvar="WTF_HEALTHCHECKS_APIKEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="apiKey", desc="Healthchecks read-only API-key", value="string" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="apiURL", desc="<em>Optional</em> Healthchecks API URL. Default: <code>https://healthchecks.io/</code>", value="string" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="tags", desc="Only show checks with tags", value="list" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="healthchecks" %}
{% include "src_path.md" %}
