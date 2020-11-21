![digitalocean](/assets/services/digitalocean.png){: align=left width=128 height=128}

# DigitalOcean

DigitalOcean module displays a list of your DigitalOcean droplets and Kubernetes clusters and allows you to interact with them in these ways:

* Destroy a droplet
* Enable private networking on a droplet
* Reboot a droplet
* Shut down a droplet
* Show info about a droplet

## Configuration

```yaml
digitalocean:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  position:
    top: 4
    left: 2
    width: 2
    height: 2
  refreshInterval: 15
  title: "🦈 DigitalOcean"
```

With explicit columns defined:

```yaml
digitalocean:
  apiKey: "p0d13*********************************************c3"
  columns:
    - Name
    - Status
    - Vcpus
    - Disk
    - Memory
    - Region.Slug
  enabled: true
  position:
    top: 4
    left: 2
    width: 2
    height: 2
  refreshInterval: 15
  title: "🦈 DigitalOcean"
```

## Screenshots

<img src="/assets/modules/digitalocean.png" class="screenshot" width="320" height="84" alt="digitalocean screenshot" />

<br />

<img src="/assets/modules/digitalocean_droplet_info.png" class="screenshot" width="320" height="197" alt="digitalocean screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="DigitalOcean", envvar="WTF_DIGITALOCEAN_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        <tr>
            <td>
                <code>columns</code>
                <br />
                <em>Optional</em> A list of the droplet attributes to display. Defines the columns displayed in the widget.
            </td>
            <td>
                Any publicly-accessible properties on a DigitalOcean <a href="https://github.com/digitalocean/godo/blob/main/droplets.go">Droplet</a>, <a href="https://github.com/digitalocean/godo/blob/main/images.go">Image</a>, <A href="https://github.com/digitalocean/godo/blob/main/regions.go">Region</a>, or <a href="https://github.com/digitalocean/godo/blob/main/sizes.go">Size</a>.
            </td>
        </tr>
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}
    
    {% set questionmark="Displays information about a droplet" %}
    {% include "keyboard/questionmark.md" %}

    {% set esc="Close the modal dialog" %}
    {% include "keyboard/esc.md" %}

    {% set return="Display information about a droplet" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set b="Reboot a droplet" %}
    {% include "keyboard/b.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set p="Enable private networking on a droplet" %}
    {% include "keyboard/p.md" %}

    {% include "keyboard/r.md" %}

    {% set s="Shut down a droplet" %}
    {% include "keyboard/s.md" %}

    {% set u="Enable private networking on a droplet" %}
    {% include "keyboard/u.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/ctrlD.md" %}

  </tbody>
</table>

{% set src="digitalocean" %}
{% include "src_path.md" %}