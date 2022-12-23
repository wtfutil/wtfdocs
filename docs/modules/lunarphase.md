# Lunar Phase

Displays the phase of the Moon as ASCII art from [Wttr.in](http://wttr.in). The width of the column in which the lunar phase is displayed needs to be large enough for the ASCII graphic to fit or multiple columns must be allocated.

## Configuration

```yaml
lunarphase:
  enabled: true
  position:
    top: 3
    left: 5
    height: 2
    width: 2
  language: 'en'
  refreshInterval: 5h
```

## Screenshots

<p float="left">
  <img class="screenshot" src="/assets/modules/lunarphase.png" width="640" height="448" alt="lunarphase screenshot" />
  <img class="screenshot" src="/assets/modules/lunarphase-fr.png" width="640" height="448" alt="lunarphase french screenshot" />
</p>

{% set src="lunarphase" %}
{% include "src_path.md" %}
