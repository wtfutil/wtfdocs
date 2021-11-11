# Have I Been Pwned (HIBP)

Indicates whether or not your listed email addresses appear in the [Have I Been Pwned](https://haveibeenpwned.com) breach database.

**Note:** As of v0.19.0, WTF requires you use a Have I Been Pwned API key to connect to the service. See details below.

## Configuration

```yaml
hibp:
  accounts:
  - test@example.com
  - pwned@gmail.com
  apiKey: "p0d13*********************************************c3"
  colors:
    ok: "green"
    pwned: "red"
  enabled: true
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 12h
  since: "2019-06-22"
```

## Screenshots

<img class="screenshot" src="/assets/modules/hibp.png" width="320" height="79" alt="hibp screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="accounts", desc="A list of the accounts to check the HIBP database for." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="DigitalOcean", envvar="WTF_DIGITALOCEAN_API_KEY" %}
            {% include "attributes/apikey.md" %}
        {% endwith %}

        {% with name="colors", desc="<em>Optional</em> The colors to display for accounts that have not been pwned and ones that have. Defaults to <code>white</code> for unpwned accounts, <code>red</code> for pwned accounts." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="since", desc="<em>Optional</em> Only check for breaches after this date. Set this if you've been breached in the past, have taken steps to mitigate that (changing passwords, cancelling accounts, etc.) and only want to know about future breaches.", value="A date string in the format 'yyyy-mm-dd', ie: '2019-06-22'" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

{% set src="hibp" %}
{% include "src_path.md" %}