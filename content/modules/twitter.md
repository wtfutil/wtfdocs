---
title: "Twitter"
date: 2018-07-31T20:21:37-07:00
draft: false
weight: 260
---

Connects to the Twitter API and displays a single user's tweets.

NOTE: This only works for single-application developer accounts for now.

To make this work, you'll need a couple of things:

1. A [Twitter developer account](https://developer.twitter.com/content/developer-twitter/en.html)
2. A [Twitter bearer token](https://developer.twitter.com/en/docs/basics/authentication/overview/application-only).

Once you have your developer account, a relatively painless way to get a
bearer token is to use [TBT](https://github.com/Trinergy/twitter_bearer_token).

## Configuration

### Single Account

```yaml
twitter:
  bearerToken: "3276d7155dd9ee27b8b14f8743a408a9"
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
  bearerToken: "3276d7155dd9ee27b8b14f8743a408a9"
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

{{% attributes %}}
  <tr>
    <td>`bearerToken`</td>
    <td>Your <a href="https://developer.twitter.com/en/docs/basics/authentication/overview/application-only.html">Twitter single-application Bearer Token</a></td>
    <td></td>
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

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `h` <br />
<span class="caption">Action:</span> Display the previous Twitter account.

<span class="caption">Key:</span> `l` <br />
<span class="caption">Action:</span> Display the next Twitter account.

<span class="caption">Key:</span> `o` <br />
<span class="caption">Action:</span> Opens the account in your local browser.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Display the previous Twitter account.

<span class="caption">Key:</span> `→ <br />
<span class="caption">Action:</span> Display the next Twitter account.

{{% sourcePath module="twitter" %}}
