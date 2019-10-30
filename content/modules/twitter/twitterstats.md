---
title: "Twitter Stats"
date: 2018-07-31T20:21:37-07:00
draft: false
weight: 40
---

Connects to the Twitter API and displays statistics about the number of tweets and followers for a set of usernames.

![](https://ameo.link/u/6o5.png)

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

```yaml
twitterstats:
  consumerKey: "3276d7155dd9ee27b8b14f8743a408a9"
  consumerSecret: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  position:
    top: 0
    left: 1
    height: 1
    width: 1
  refreshInterval: 20000
  screenNames:
  - "wtfutil"
  - "dril"
```

{{% attributes %}}
  <tr>
    <td>`bearerToken`</td>
    <td>_Optional_ Your <a href="https://developer.twitter.com/en/docs/basics/authentication/overview/application-only.html">Twitter single-application Bearer Token.  This must be supplied if `consumerKey` and `consumerSecret` are not.</a></td>
    <td></td>
  </tr>
  <tr>
    <td>`consumerKey`</td>
    <td>_Optional_ Your Twitter Consumer API secret.  This must be supplied along with `consumerSecret` if `bearerToken` isn't supplied.</a></td>
    <td></td>
  </tr>
  <tr>
    <td>`consumerSecret`</td>
    <td>_Optional_ Your Twitter Consumer API key.  This must be supplied along with `consumerKey` if `bearerToken` isn't supplied.</td>
    <td></td>
  </tr>

  {{< attributes/border >}}
  {{< attributes/custom name="count" desc="_Optional_ The number of tweets to return per account. Default: 5." value="Any positive integer" >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="screenNames" desc="The screen names of the Twitter users who's tweets you want to follow." value="A list of any valid Twitter user's screen names" >}}
{{% /attributes %}}
