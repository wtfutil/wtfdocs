# Airbrake

Displays error information about your Airbrake project. Provides the ability to
mute/unmute errors or resolve them.

## Configuration

```yaml
airbrake:
  enabled: true
  projectID: 123
  authToken: "123**********************2b9"
  position:
    top: 4
    left: 0
    width: 3
    height: 1
  refreshInterval: 60
```

## Screenshots

<img src="/assets/modules/airbrake.png" class="screenshot"  width="578" height="176" alt="airbrake screenshot" />

## Attributes


<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>projectID</code>
        <br />
        An ID of the project at Airbrake
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>authToken</code>
        <br />
        A user token, which grants access to the Airbrake API (you can find it in your profile).
    </td>
    <td></td>
</tr>
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="View information about the selected error" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set o="Open the selected story in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/j.md" %}
    {% include "keyboard/k.md" %}

    {% set s="Resolves the selected error on Airbrake" %}
    {% include "keyboard/s.md" %}

    {% set m="Mutes the selected error on Airbrake" %}
    {% include "keyboard/m.md" %}

    {% set u="Unmutes the selected error on Airbrake" %}
    {% include "keyboard/u.md" %}

    {% include "keyboard/r.md" %}

    {% set t="Switches the display mode between normal and 'compare' views" %}
    {% include "keyboard/t.md" %}

    {% include "keyboard/spacer.md" %}

    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}

  </tbody>
</table>

{% set src="airbrake" %}
{% include "src_path.md" %}
