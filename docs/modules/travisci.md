# TravicCI

Displays build information for your Travis CI account.

## Configuration

This module pulls information from <code>api.travis-ci.com</code> (when <code>pro: true</code>) or <code>api.travis-ci.org</code> (when <code>pro: false</code>).

```yaml
travisci:
  apiKey: "p0d13*********************************************c3"
  enabled: true
  compact: true
  limit: 8
  sort_by: "id:desc"
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  pro: false
  refreshInterval: 15m
```

## Screenshots

<img class="screenshot" src="/assets/modules/travisci.png" width="640" height="187" alt="travisci screenshot" />

## Attributes

<table>
  {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="TravisCI", envvar="WTF_TRAVIS_API_TOKEN" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="baseURL", desc="<em>Optional</em> Your TravisCI Enterprise API URL.", value="A valid URL. Can also be set via the <code>WTF_TRAVIS_BASE_URL</code> environment variable." %}
          {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="compact", desc="<em>Optional</em> When true, displays one line per build entry. When false, displays two lines per entry. Default: <code>false</code>", value="<code>true</code>, <code>false</code>" %}
          {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="sort_by", desc="<em>Optional</em> Sortable by: id, created_at, started_at, finished_at, number, append :desc to any attribute to reverse order. The default value is <code>id:desc</code>. See <a href='https://developer.travis-ci.com/resource/builds'>https://developer.travis-ci.com/resource/builds</a> for more information.", value="" %}
          {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="pro", desc="<em>Optional</em> Determines whether or not this module will use the Pro version of Travis CI.", value="<code>true</code>, <code>false</code>" %}
          {% include "attributes/custom.md" %}
        {% endwith %}

    </tbody>
</table>

{% set src="travisci" %}
{% include "src_path.md" %}