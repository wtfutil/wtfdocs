# Lunar Phase

Displays the phase of the Moon as ASCII art from [Wttr.in](http://wttr.in).

## Configuration

```yaml
lunarphase:
  enabled: true
  position:
    top: 3
    left: 5
    height: 2
    width: 1
  language: 'en'
  refreshInterval: 5h
```

## Screenshots

<p float="left">
  <img class="screenshot" src="/assets/modules/lunarphase.png" width="320" height="640" alt="lunarphase screenshot" />
  <img class="screenshot" src="/assets/modules/lunarphase-fr.png" width="320" height="640" alt="lunarphase french screenshot" />
</p>

{% set src="lunarphase" %}
{% include "src_path.md" %}
