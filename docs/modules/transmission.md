![transmission](/assets/services/transmission.png){: align=left width=128 height=128}

# Transmission

View and manage your [Transmission](https://transmissionbt.com) bittorrent daemon. This widget shows you the currently-loaded 
torrents, their "download complete" percentage, and their seeding status.

## Configuration

```yaml
transmission:
  enabled: true
  host: "192.168.1.5"
  password: "passwordpassword"
  position:
    top: 4
    left: 3
    width: 2
    height: 1
  refreshInterval: 3
  username: "transmission"
```

## Screenshots

<img class="screenshot" src="/assets/modules/transmission.png" width="320" height="190" alt="transmission screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="host", desc="The IP address of the machine that your Transmission daemon is running on.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% set service="Transmission" %}
        {% set pwdesc="The password you use to connect to your Transmission daemon." %}
        {% include "attributes/password.md" %}

        {% set service="Transmission" %}
        {% set undesc="The username you use to connect to your Transmission daemon." %}
        {% include "attributes/username.md" %}
    </tbody>
</table>

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Pause/resume the selected torrent" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}
    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/ctrlD.md" %}
  </tbody>
</table>

{% set src="transmission" %}
{% include "src_path.md" %}