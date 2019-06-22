---
title: "Have I Been Pwned (HIBP)"
date: 2019-06-22T15:47:08-04:00
draft: false
weight: 125
---

<img class="screenshot" src="/imgs/modules/hibp.png" width="320" height="79" alt="hibp screenshot" />

Indicates whether or not your listed email addresses appear in the [Have I Been Pwned](https://haveibeenpwned.com) breach database.

## Configuration

```yaml
hibp:
  accounts:
  - test@example.com
  - pwned@gmail.com
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

### Attributes

`accounts` <br />
A list of the accounts to check the HIBP database for. 

`colors` <br />
_Optional_ The colors to display for accounts that have not been pwned and ones that have. Defaults to 
"white" for unpwned accounts, "red" for pwned accounts.

`enabled` <br />
Whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
**Note:** This module enforces a minimum refresh interval of 21600 seconds to keep from hitting 
the HIBP API needlessly. Setting a value below this minimum will  have no effect. <br />
Values: A positive integer, `0..n`.

`since` <br />
_Optional_ Only check for breaches after this date. Set this if you've been breached in the past, 
have taken steps to mitigate that (changing passwords, cancelling accounts, etc.) and now only 
want to know about future breaches. <br />
Values: A date string in the format "yyyy-mm-dd", ie: "2019-06-22"