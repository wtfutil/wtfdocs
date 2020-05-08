---
title: "Pretty Weather"
date: 2018-06-02T05:32:04-07:00
draft: false
weight: 10
---

<img class="screenshot" src="/imgs/modules/prettyweather.png" width="320" height="191" alt="prettyweather screenshot" />

Displays weather information as ASCII art from [Wttr.in](http://wttr.in).

Consider using wego directly, to avoid issues with rate limiting.
See [wego](../../cmdrunner/wego).

## Configuration

{{< code lang="yaml" >}}
    prettyweather:
      enabled: true
      city: "tehran"
      position:
        top: 3
        left: 5
        height: 1
        width: 1
      refreshInterval: 300
      unit: "m"
      view: 0
      language: "en"
{{< /code >}}

{{% attributes %}}
  {{< attributes/border >}}

  <tr>
    <td>`city`</td>
    <td>_Optional_ The name of the city to display weather for. Default: Barcelona.</td>
    <td>The name of any city supported by [Wttr.in](http://wttr.in)</td>
  </tr>

  {{< attributes/enabled >}}

  {{< attributes/custom name="language" desc="_Optional_ Wttr.in language configuration. Default: en." value="See `curl wttr.in/:translation` for more details" >}}

  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

  {{< attributes/custom name="unit" desc="_Optional_ The scale to display temperatures in. Default: m." value="`u` for Fahrenheit, `m` for Celsius" >}}
  {{< attributes/custom name="view" desc="_Optional_ Wttr.in view configuration." value="See `curl wttr.in/:help` for more details" >}}
{{% /attributes %}}

<<<<<<< HEAD
{{% sourcePath module="weatherservices/prettyweather" %}}
=======
## Source Code

{{< code lang="bash" >}}
wtf/modules/weatherservices/prettyweather/
{{< /code >}}
>>>>>>> Fix syntax highlighting
