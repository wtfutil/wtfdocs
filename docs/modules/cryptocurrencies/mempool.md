# Mempool

Get the current sat/vB prices to use for Bitcoin transactions using [Mempool](https://mempool.space/).

## Configuration

```yaml
mempool:
    enabled: true
    border: false
    position:
    top: 1
    left: 0
    width: 9 # 18 characters
    height: 4 # 4 characters
    refreshInterval: 120
```

## Screenshots

<img class="screenshot" src="/assets/modules/mempool.png" width="300" height="400" alt="mempool screenshot" />

{% set src="cryptoexchanges/mempool" %}
{% include "src_path.md" %}