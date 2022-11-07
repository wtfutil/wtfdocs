# Urlcheck

Checks if your URLs are responding.

This module will continously request the headers for a given list of URLs and then displays theirs status codes. 

## Configuration

```yaml
urlcheck:
  enabled: true
  timeout: 25
  urls:
    - http://go.dev                   # ok
    - https://wtfutil.com             # ok
    - wtfutil.com                     # invalid url
    - http://www.nope.nope            # dns error
    - https://httpbin.org/status/500  # Internal server error
  position:
    top: 0
    left: 0
    height: 1
    width: 1
  refreshInterval: 30
```

## Screenshots

<img src="/assets/modules/url_check.png" class="screenshot" width="600" height="273" alt="urlcheck screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        <tr>
            <td>
                <code>timeout</code>
                <br />
                <em>Optional</em> The amountof time allowed to a single request to complete. Default: <code>30</code>.
                
            </td>
            <td>A positive integer.</td>
        </tr>
        <tr>
            <td>
                <code>urls</code>
                <br />
                <em>Required</em> The URLs to be requested. The protocol is required too (Ex.: http://go.dev).
            </td>
            <td>A list of strings.</td>
        </tr>
    </tbody>
</table>

## Logging

These events will be logged in the standard logger:
 * Timeouts,
 * DNS lookup errors,
 * other generals Request errors. 

{% set src="urlcheck" %}
{% include "src_path.md" %}