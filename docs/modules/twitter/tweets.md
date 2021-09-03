# Twitter Tweets

Connects to the Twitter API and displays a single user's tweets.

NOTE: This only works for single-application developer accounts for now.

To make this work, you'll need a couple of things:

1. [Twitter developer account](https://developer.twitter.com/content/developer-twitter/en.html)

and one of the following:

a) [Twitter bearer token](https://developer.twitter.com/en/docs/basics/authentication/overview/application-only)<br/>
b) [Consumer API keys](https://developer.twitter.com/en/docs/basics/authentication/guides/access-tokens)

You must have either a bearer token or consumer key + consumer secret provided.  To get the consumer API keys, you must first create a Twitter application.  Then, go to the "Keys and tokens" page and copy the API key and API secret key under the Consumer API keys section.

Once you have your developer account, a relatively painless way to get a
bearer token is to use [TBT](https://github.com/Trinergy/twitter_bearer_token).

## Configuration

### Single Account

```yaml
twitter:
  bearerToken: "d23*******************************************3r2"
  count: 5
  enabled: true
  position:
    top: 0
    left: 1
    height: 1
    width: 1
  refreshInterval: 20000
  screenName: "wtfutil"
```

### Multiple Accounts

```yaml
twitter:
  bearerToken: "d23*******************************************3r2"
  count: 5
  enabled: true
  position:
    top: 0
    left: 1
    height: 1
    width: 1
  refreshInterval: 20000
  screenNames:
  - "golang"
  - "wtfutil"
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="bearerToken", desc="<em>Optional</em> Your <a href='https://developer.twitter.com/en/docs/basics/authentication/overview/application-only.html'>Twitter single-application Bearer Token</a>.  This must be supplied if <code>consumerKey</code> and <code>consumerSecret</code> are not.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="consumerKey", desc="<em>Optional</em> Your Twitter Consumer API secret. This must be supplied along with <code>consumerSecret</code> if <code>bearerToken</code> isn't supplied.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="consumerSecret", desc="<em>Optional</em> Your Twitter Consumer API key. This must be supplied along with <code>consumerKey</code> if <code>bearerToken</code> isn't supplied.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="count", desc="<em>Optional</em> The number of tweets to return per account. Default: <code>5</code>.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="screenNames", desc="The screen names of the Twitter users who's tweets you want to follow.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set return="Open the current Twitter account in the browser" %}
    {% include "keyboard/return.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Show the previous Twitter account" %}
    {% include "keyboard/h.md" %}

    {% set l="Show the next Twitter account" %}
    {% include "keyboard/l.md" %}

    {% set o="Open the current Twitter account in the browser" %}
    {% include "keyboard/o.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous Twitter account" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next Twitter account" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="twitter" %}
{% include "src_path.md" %}