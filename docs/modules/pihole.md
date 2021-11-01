![pihole](/assets/services/pihole.png){: align=left width=128 height=128}

# Pihole

Displays information about a running [Pi-hole](https://pi-hole.net/) server.

## Configuration

```yaml
pihole:
  apiUrl: http://192.168.1.100:1010/admin/api.php
  enabled: true
  maxClientWidth: 20
  maxDomainWidth: 20
  position:
    top: 5
    left: 0
    height: 2
    width: 2
  refreshInterval: 1m
  showSummary: true
  showTopItems: 5
  showTopClients: 5
  token: atvvedmpyat8140rnhodrok3qr58d8ph85wl6wk1rpb9upiwx1tl6eittz403pqaj
```

## Screenshots

<img class="screenshot" src="/assets/modules/pihole.png" width="688" height="420" alt="Pi-hole screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="apiUrl", desc="The Pi-Hole API Server URL. Typically: <code>http://<ip:port>/admin/api.php</code>", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

         {% with name="maxClientWidth", desc="<em>Optional</em> Number of characters to display when outputting query and ad domain names. Default: <code>20</code>", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="maxDomainWidth", desc="<em>Optional</em> Number of characters to display when outputting client name and IP. Default: <code>20</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showSummary", desc="Show summary. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showTopItems", desc="<em>Optional</em> Number of Top Queries and Top Ads to display. 0 disables the output. Default: <code>5</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showTopClients", desc="<em>Optional</em> Number of Top Sources and Query Types to display. 0 disables the output. Default: <code>5</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="token", desc="Navigate to http://<ip:port>/admin/settings.php?tab=api and choose 'Show API Token'", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="pihole" %}
{% include "src_path.md" %}