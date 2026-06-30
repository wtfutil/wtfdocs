# Mempool

Get the current sat/vB prices to use for Bitcoin transactions using [Mempool](https://mempool.space/).

## Configuration

### Without borders
`width` x `height`: 18 chars x 4 chars

### With borders
20 chars x 6 chars

```yaml
mempool:
    enabled: true
    border: false
    position:
        top: 1
        left: 0
        width: 9 
        height: 4
    refreshInterval: 120
```

## Screenshots

<img class="screenshot" src="/assets/modules/mempool.png" width="300" height="400" alt="mempool screenshot" />


## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="apiURL", desc="The API to pull data from.", value="https://mempool.space/api/v1/fees/recommended" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="cryptoexchanges/mempool" %}
{% include "src_path.md" %}
