# IP-API

Displays your current IP address information, from [IP-API.com](http://ip-api.com).

**Note:** IP-API.com has a free-plan rate limit of 120 requests per
minute.

## Configuration

```yaml
ipapi:
  colors:
    name: red
    value: white
  # Optional  
  args:
    - "ip"
    - "isp"
    - "as"
    - "city"
    - "regionName"
    - "country"
    - "continent"
    - "coordinates"
    - "organization"
    - "timezone"
    - "reverseDNS"
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 150s
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="colors.name", desc="<em>Optional</em> The default colour for the row names." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        {% with name="colors.value", desc="<em>Optional</em> The default colour for the row values." %}
            {% include "attributes/colors/custom.md" %}
        {% endwith %}

        <tr>
            <td>
                <code>args</code>
                <br />
                <em>Optional</em> The data to display and the order to display it in.
            </td>
            <td>
                <a href="#args">See args table below.</a>
            </td>
        </tr>
    </tbody>
</table>

## Args

<table>
    <thead>
        <tr>
            <th>Value</th>
            <th>Description</th>
            <th>Example</th>
        </tr>
    <tbody>
        <tr>
            <td>
                <code>ip</code>
            </td>
            <td>
                IP address
            </td>
            <td>
                <code>173.194.67.94</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>isp</code>
            </td>
            <td>
                ISP name
            </td>
            <td>
                <code>Google</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>as</code>
            </td>
            <td>
                AS number and organization, separated by space (RIR). Empty for IP blocks not being announced in BGP tables.
            </td>
            <td>
                <code>AS15169 Google Inc.</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>asName</code>
            </td>
            <td>
                AS name (RIR). Empty for IP blocks not being announced in BGP tables.
            </td>
            <td>
                <code>GOOGLE</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>district</code>
            </td>
            <td>
                District (subdivision of city)
            </td>
            <td>
                <code>Old Farm District</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>city</code>
            </td>
            <td>
                City
            </td>
            <td>
                <code>Mountain View</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>region</code>
            </td>
            <td>
                Region/state short code (FIPS or ISO)
            </td>
            <td>
                <code>CA</code> or <code>10</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>regionName</code>
            </td>
            <td>
                Region/state
            </td>
            <td>
                <code>California</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>country</code>
            </td>
            <td>
                Country name
            </td>
            <td>
                <code>United States</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>countryCode</code>
            </td>
            <td>
                Two-letter country code <a href="https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2">ISO 3166-1 alpha-2</a>
            </td>
            <td>
                <code>US</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>continent</code>
            </td>
            <td>
                Continent name
            </td>
            <td>
                <code>North America</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>continentCode</code>
            </td>
            <td>
                Two-letter continent code
            </td>
            <td>
                <code>NA</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>coordinates</code>
            </td>
            <td>
                Latitude and longitude
            </td>
            <td>
                <code>37.4192, -122.0574</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>postalCode</code>
            </td>
            <td>
                Postal code
            </td>
            <td>
                <code>94043</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>currency</code>
            </td>
            <td>
                National currency
            </td>
            <td>
                <code>USD</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>organization</code>
            </td>
            <td>
                Organization name
            </td>
            <td>
                <code>Google</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>timezone</code>
            </td>
            <td>
                Timezone (tz)
            </td>
            <td>
                <code>America/Los_Angeles</code>
            </td>
        </tr>
        <tr>
            <td>
                <code>reverseDNS</code>
            </td>
            <td>
                Reverse DNS of the IP
            </td>
            <td>
                <code>wi-in-f94.1e100.net</code>
            </td>
        </tr>
    </tbody>
</table>

{% set src="ipaddresses/ipapi" %}
{% include "src_path.md" %}