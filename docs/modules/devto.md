# DEV

Displays stories from [The Practical DEV](https://dev.to).

## Configuration

```yaml
devto:
  enabled: true
  numberOfArticles: 10
  position:
    top: 1
    left: 1
    height: 1
    width: 2
  contentTag: "showdev" 
  contentUsername: "victoravelar"
  contentState: "rising"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>contentTag</code>
        <br />
        <em>Optional</em> List articles from a specific tag.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>contentUsername</code>
        <br />
        <em>Optional</em> List articles from a specific user.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>contentState</code>
        <br />
        <em>Optional</em> Alters the feed output.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>numberOfArticles</code>
        <br />
        <em>Optional</em> Defines number of articles to be displayed. Default: <code>10</code>.
    </td>
    <td>Any positive integer < 20.</td>
</tr>
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set esc="Cancel the selection" %}
    {% include "keyboard/esc.md" %}

    {% set return="Open the selected story in the browser" %}
    {% include "keyboard/return.md" %}
   
    {% include "keyboard/spacer.md" %}
    
    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="devto" %}
{% include "src_path.md" %}