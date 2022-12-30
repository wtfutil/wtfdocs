# Lunar Phase

Displays the phase of the Moon as ASCII art from [Wttr.in](http://wttr.in).

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
  title: 'Phase of the Moon'
  timeout: 30
```

The width of the column in which the lunar phase is displayed needs to be
large enough for the ASCII graphic to fit or multiple columns must be allocated.
For example:

```yaml
grid:
    columns: [74, 12]
    rows: [14, 14]
```

The default `wtf` settings for opening a URL in a browser on Linux is
to open the URL with `xdg-open`. However, `xdg-open` depends on the KDE
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

To use module keyboard controls, first press the number of the module
displayed in the title of the module widget to give focus to that module.
To leave module keyboard control mode, press `Esc`.

When using keyboard controls to change the lunar phase day, the
`lunarphase` module widget title will be updated to reflect the currently
configured lunar phase day but the module widget will not automatically refresh.
After selecting the desired day using keyboard controls, refresh the module
widget by pressing `r`. For example, to display next week's lunar phase,
press `Up Arrow` or `N` then press `r`. To view the lunar phase 2 days
previous to the current day, press `Left Arrow` or `p` twice then press `r`.

The following keyboard controls are supported in the `lunarphase` module:

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

    {% set t="Display today's lunar phase" %}
    {% include "keyboard/t.md" %}

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
