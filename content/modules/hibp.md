---
title: "Have I Been Pwned (HIBP)"
date: 2019-06-22T15:47:08-04:00
draft: false
weight: 125
---

<img class="screenshot" src="/imgs/modules/hibp.png" width="320" height="79" alt="hibp screenshot" />

Indicates whether or not your listed email addresses appear in the [Have I Been Pwned](https://haveibeenpwned.com) breach database.

**Note:** As of v0.19.0, WTF requires you use a Have I Been Pwned API key to conenct to the service. See details below.

## Configuration

```yaml
hibp:
  accounts:
  - test@example.com
  - pwned@gmail.com
  apiKey: "ef9cb8d7-0941-4633-b056-3bobcatd3c78"
  colors:
    ok: "green"
    pwned: "red"
  enabled: true
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 43200
  since: "2019-06-22"
```

{{% attributes %}}
  {{< attributes/custom name="accounts" desc="A list of the accounts to check the HIBP database for." >}}
  {{< attributes/apikey name="Have I Been Pwned" link="https://haveibeenpwned.com/API/Key" envvar="WTF_HIBP_TOKEN" >}}
  {{< attributes/custom name="colors" desc="_Optional_ The colors to display for accounts that have not been pwned and ones that have. Defaults to `white` for unpwned accounts, `red` for pwned accounts." >}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  {{< attributes/custom name="since" desc="_Optional_ Only check for breaches after this date. Set this if you've been breached in the past, have taken steps to mitigate that (changing passwords, cancelling accounts, etc.) and only want to know about future breaches." value="A date string in the format 'yyyy-mm-dd', ie: '2019-06-22'" >}}
{{% /attributes %}}

{{% sourcePath module="hibp" %}}