![weather](/assets/services/weather.jpg){: align=left width=128 height=128}

# Weather

Displays current weather reports, including current temperature, sunrise time, and sunset time.

## Configuration

```yaml
weather:
  apiKey: "p0d13*********************************************c3"
  # From http://bulk.openweathermap.org/sample/city.list.json.gz
  cityids:
  - 6173331
  - 3128760
  - 6167865
  - 6176823
  colors:
    current: "lightblue"
  enabled: true
  language: "EN"
  position:
    top: 0
    left: 2
    height: 1
    width: 1
  refreshInterval: 900
  tempUnit: "C"
  useEmoji: true
```

## Screenshots

![Weather](/assets/modules/weather.png)

## Attributes

<table>
  {% include "attributes/table_header.md" %}

  <tbody>
    {% with name="OpenWeatherMap", envvar="WTF_OWM_API_KEY" %}
        {% include "attributes/apikey.md" %}
    {% endwith %}

    <tr>
        <td>
            <code>cityids</code>
            <br />
            A list of the <a href="http://bulk.openweathermap.org/sample/city.list.json.gz">OpenWeatherMap city IDs</a> for the cities you want to view.
        </td>
        <td>A list of positive integers.</td>
    </tr>
    <tr>
        <td>
            <code>colors.current</code>
            <br />
            <em>Optional</em> The color to highlight the current temperature in. Default: <code>green</code>.
        </td>
        <td></td>
    </tr>
    <tr>
        <td>
            <code>language</code>
            <br />
            <em>Optional</em> The human language in which to present the weather data. Default: <code>EN</code>.
        </td> 
        <td>
            Any <a href="https://openweathermap.org/current">language identifier</a> specified by OpenWeatherMap.
        </td>
    </tr>
    <tr>
        <td>
            <code>tempUnit</code>
            <br />
            <em>Optional</em> The temperature scale in which to display temperature values. Default: <code>C</code>.
        </td>
        <td><code>F</code> for Fahrenheit, <code>C</code> for Celcius</td>
    </tr>
    <tr>
        <td>
            <code>useEmoji</code>
            <br />
            <em>Optional</em> Whether or not to display emoji characters in the title. Default: <code>true</code>.
        </td>
        <td><code>true</code>, <code>false</code></td>
    </tr>
  </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Show the previous weather location" %}
    {% include "keyboard/h.md" %}

    {% set l="Show the next weather location" %}
    {% include "keyboard/l.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowback="Show the previous weather location" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowfore="Show the next weather location" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="weatherservices/weather" %}
{% include "src_path.md" %}
