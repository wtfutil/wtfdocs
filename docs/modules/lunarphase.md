# Lunar Phase

Displays the phase of the Moon as ASCII art from [Wttr.in](http://wttr.in). The width of the column in which the lunar phase is displayed needs to be large enough for the ASCII graphic to fit or multiple columns must be allocated.

## Configuration

```yaml
lunarphase:
  enabled: true
  language: 'en'
  position:
    top: 3
    left: 5
    height: 2
    width: 2
  refreshInterval: 5h
  title: 'Phase of the Moon'
  timeout: 30
```

## Screenshots

<p float="left">
  <img class="screenshot" src="/assets/modules/lunarphase.png" width="640" height="448" alt="lunarphase screenshot" />
  <img class="screenshot" src="/assets/modules/lunarphase-fr.png" width="640" height="448" alt="lunarphase french screenshot" />
</p>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}
    
    {% set return="Open selected day lunar phase at nineplanets.org in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set n="Display next day lunar phase" %}
    {% include "keyboard/n.md" %}

    {% set p="Display previous day lunar phase" %}
    {% include "keyboard/p.md" %}

    {% set N="Display next week lunar phase" %}
    {% include "keyboard/N.md" %}

    {% set P="Display previous week lunar phase" %}
    {% include "keyboard/P.md" %}

    {% set o="Open selected day lunar phase at nineplanets.org in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous day lunar phase" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next day lunar phase" %}
    {% include "keyboard/arrowFore.md" %}

    {% set customArrowDown="Show previous week lunar phase" %}
    {% include "keyboard/customArrowDown.md" %}

    {% set customArrowUp="Show next week lunar phase" %}
    {% include "keyboard/customArrowUp.md" %}

    {% include "keyboard/spacer.md" %}

    {% set customCtrlD="Toggle disable/enable widget display" %}
    {% include "keyboard/customCtrlD.md" %}
  </tbody>
</table>

{% set src="lunarphase" %}
{% include "src_path.md" %}
