---
title: "Weather"
date: 2018-05-09T11:44:13-07:00
draft: false
weight: 20
---

<img class="screenshot" src="/imgs/modules/weather.png" width="320" height="187" alt="weather screenshot" />

Displays a configurable list of current weather report, including current temperature, sunrise time, and sunset time.

## Configuration

```yaml
weather:
  apiKey: "p0d13*********************************************c3"
  # From http://openweathermap.org/help/city_list.txt
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
```
{{% attributes %}}
  {{< attributes/apikey name="OpenWeatherMap" link="https://openweathermap.org/appid" envvar="WTF_OWM_API_KEY" >}}
  {{< attributes/border >}}

  <tr>
    <td>`cityids`</td>
    <td>A list of the <a href="http://openweathermap.org/help/city_list.txt">OpenWeatherMap city IDs</a> for the cities you want to view.</td>
    <td>A list of positive integers</td>
  </tr>

  {{< attributes/colors/custom name="colors.current" desc="_Optional_ The color to highlight the current temperature in. Default: green." >}}

  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}

  <tr>
    <td>`language`</td>
    <td>_Optional_ The human language in which to present the weather data. Default: EN.</td> 
    <td>Any <a href="https://openweathermap.org/current">language identifier</a> specified by OpenWeatherMap"</td>
  </tr>

  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

  {{< attributes/custom name="tempUnit" desc="_Optional_ The temperature scale in which to display temperature values. Default: C." value="`F` for Fahrenheit, `C` for Celcius" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous weather location" >}}
  {{< keyboard/l desc="Show the next weather location" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous Twitter account" >}} 
  {{< keyboard/arrowFore desc="Show the next Twitter account" >}}
{{% /keyboard %}}

## Source Code

```bash
wtf/modules/weatherservices/weather/
```
