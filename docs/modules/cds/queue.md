# CDS Queue

Display current [CDS](https://ovh.github.io/cds/) queue - waiting or building jobs.

## Configuration

```yaml
cdsQueue:
  enabled: true
  position:
    top: 0
    left: 0
    height: 3
    width: 2
  refreshInterval: 8
  apiURL: https://api.cds.localhost.local
  token: xxxxxxxxxxxx
```

## Screenshots

<img class="screenshot" src="/assets/modules/cds_queue.png" width="520" alt="CDS Queue screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
       <tr>
            <td>
                <code>apiURL</code>
                <br />
                Your CDS API URL.
            </td>
            <td></td>
        </tr>
        <tr>
            <td>
                <code>token</code>
                <br />
                Your CDS Consumer Token.
            </td>
            <td></td>
        </tr> 
    </tbody>
</table>

{% set src="cds/queue/" %}
{% include "src_path.md" %}