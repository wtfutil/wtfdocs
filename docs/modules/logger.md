# Logger

View contents of wtf log file (~/.config/wtf/log.txt).

## Configuration

```yaml
logger:
  enabled: true
  colors:
    label: "green"
    text: "white"
  position:
    top: 1
    left: 2
    height: 1
    width: 2
  refreshInterval: 15
``` 

## Screenshots

<img src="/assets/modules/logger.png" class="screenshot" width="600" height="150" alt="logger screenshot" />

{% set src="logger" %}
{% include "src_path.md" %}