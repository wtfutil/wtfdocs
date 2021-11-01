# ARPANSA

Displays Ultraviolet radiation index information from ARPANSA for an Australian city to help determine what level of sun protection or avoidance is necessary.

The [Australian Radiation Protection and Nuclear Safety Agency](https://www.arpansa.gov.au) (ARPANSA) is the Australian Government's primary authority on radiation protection and nuclear safety.

Interpreting the information:

* Index is specified in units of [Standard Erthermal Dose](https://www.arpansa.gov.au/services/monitoring/ultraviolet-radiation-monitoring/ultraviolet-radiation-dose/ultraviolet).
* If the UV index is less than 3 you can safely stay outdoors with minimal protection.
* If the UV index is 3 or more: wear sun protective clothing, a hat, sunglasses, sunscreen, seek shade.

## Configuration

```yaml
arpansagovau:
    enabled: true
    locationid: "Sydney"
    position:
        top: 0
        left: 0
        height: 1
        width: 1
    refreshInterval: 15m
```

<img class="screenshot" src="/assets/modules/arpansa.png" width="350" height="150" alt="arpansagovau module screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="locationid", desc="One of the <a href='https://uvdata.arpansa.gov.au/xml/uvvalues.xml'>ARPANSA</a> location ids as seen on the id attribute of the location tag. e.g. 'Sydney'", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="weatherservices/arpansagovau" %}
{% include "src_path.md" %}