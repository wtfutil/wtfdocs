# CDS Favorites

Display runs of you [CDS](https://ovh.github.io/cds/) favorites workflows.

## Configuration

```yaml
cdsFavorites:
  enabled: true
  position:
    top: 0
    left: 0
    height: 2
    width: 2
  refreshInterval: 8s
  apiURL: https://api.cds.localhost.local
  token: xxxxxxxxxxxx
  hideTags:
  - "git.repository"
  - "git.hash"
  - "triggered_by"
```

## Screenshots

<img class="screenshot" src="/assets/modules/cds_favorites.png" width="520" alt="CDS Favorites screenshot" />

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
        <tr>
            <td>
                <code>hideTags</code>
                <br />
                A CDS Runs can have many "cds tags". You can hide some tags displayed.
            </td>
            <td></td>
        </tr>
    </tbody>
</table>

{% set src="cds/favorites/" %}
{% include "src_path.md" %}