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

**[Note:]** The default `wtf` settings for opening a URL in a browser on Linux
is to open the URL with `xdg-open`. However, `xdg-open` depends on the KDE
`konqueror` web browser on many systems. An alternate configuration on Linux
systems where `xdg-open` fails or is unavailable may be necessary. One such
configuration uses the Gnome `gio` utility. To use `gio` to open URLs, add
the following to your `wtf` YAML configuration:

```yaml
openUrlUtil:
    - 'gio'
    - 'open'
```

## Screenshots

<p float="left">
  <img class="screenshot" src="/assets/modules/lunarphase.png" width="640" height="448" alt="lunarphase screenshot" />
  <img class="screenshot" src="/assets/modules/lunarphase-fr.png" width="640" height="448" alt="lunarphase french screenshot" />
</p>

## Keyboard

**[Note:]** When using keyboard controls to change the lunar phase day,
the `lunarphase` module widget title will be updated to reflect the currently
configured lunar phase day but the module widget will not automatically refresh.
After selecting the desired day using keyboard controls, refresh the module
widget by pressing `r`. For example, to display next week's lunar phase,
press `Up Arrow` or `N` then press `r`. To view the lunar phase 2 days
previous to the current day, press `Left Arrow` or `p` twice then press `r`.

To view additional informaton in a browser on the lunar phase of the day
displayed in the module widget title, press `o` or `Enter`.

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
