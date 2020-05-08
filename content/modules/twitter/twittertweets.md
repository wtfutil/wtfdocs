---
title: "Twitter"
date: 2018-07-31T20:21:37-07:00
draft: false
weight: 50
---

Connects to the Twitter API and displays a single user's tweets.

NOTE: This only works for single-application developer accounts for now.

To make this work, you'll need a couple of things:

1. A [Twitter developer account](https://developer.twitter.com/content/developer-twitter/en.html)

... and one of the following:

a) A [Twitter bearer token](https://developer.twitter.com/en/docs/basics/authentication/overview/application-only)<br/>
b) [Consumer API keys](https://developer.twitter.com/en/docs/basics/authentication/guides/access-tokens)

You must have either a bearer token or consumer key + consumer secret provided.  To get the consumer API keys, you must first create a Twitter application.  Then, go to the "Keys and tokens" page and copy the API key and API secret key under the Consumer API keys section:

![](https://ameo.link/u/6p1.png)

Once you have your developer account, a relatively painless way to get a
bearer token is to use [TBT](https://github.com/Trinergy/twitter_bearer_token).

## Configuration

### Single Account

{{< code lang="yaml" >}}
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
{{< /code >}}

### Multiple Accounts

{{< code lang="yaml" >}}
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
{{< /code >}}

{{% attributes %}}
  <tr>
    <td>`bearerToken`</td>
    <td>_Optional_ Your <a href="https://developer.twitter.com/en/docs/basics/authentication/overview/application-only.html">Twitter single-application Bearer Token</a>.  This must be supplied if `consumerKey` and `consumerSecret` are not.</td>
    <td>Leave empty to use the `WTF_TWITTER_BEARER_TOKEN` environment variable.</td>
  </tr>
  <tr>
    <td>`consumerKey`</td>
    <td>_Optional_ Your Twitter Consumer API secret.  This must be supplied along with `consumerSecret` if `bearerToken` isn't supplied.</a></td>
    <td>Leave empty to use the `WTF_TWITTER_CONSUMER_KEY` environment variable.</td>
  </tr>
  <tr>
    <td>`consumerSecret`</td>
    <td>_Optional_ Your Twitter Consumer API key.  This must be supplied along with `consumerKey` if `bearerToken` isn't supplied.</td>
    <td>Leave empty to use the `WTF_TWITTER_CONSUMER_SECRET` environment variable.</td>
  </tr>

  {{< attributes/border >}}
  {{< attributes/custom name="count" desc="_Optional_ The number of tweets to return per account. Default: 5." value="Any positive integer" >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="screenName" desc="The screen name of the Twitter user who's tweets you want to follow." value="Any valid Twitter user's screen name" >}}
  {{< attributes/custom name="screenNames" desc="The screen names of the Twitter users who's tweets you want to follow." value="A list of any valid Twitter user's screen names" >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}
  {{< keyboard/return desc="Open the current Twitter account in the browser" >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous Twitter account" >}}
  {{< keyboard/l desc="Show the next Twitter account" >}}
  {{< keyboard/o desc="Open the current Twitter account in the browser" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous Twitter account" >}}
  {{< keyboard/arrowFore desc="Show the next Twitter account" >}}
{{% /keyboard %}}

{{% sourcePath module="twitter" %}}