---
title: "New Relic"
date: 2018-05-09T09:01:14-07:00
draft: false
weight: 160
---

<img class="screenshot" src="/imgs/modules/newrelic.png" width="640" height="189" alt="newrelic screenshot" />

Connects to the New Relic API and displays the last n deploys of the
monitored applications: deploy ID, deploy time, and who deployed it.

## Keyboard Commands

<span class="caption">Key:</span> `/` <br />
<span class="caption">Action:</span> Open/close the widget's help window.

<span class="caption">Key:</span> `←` <br />
<span class="caption">Action:</span> Show the previous application.

<span class="caption">Key:</span> `→` <br />
<span class="caption">Action:</span> Show the next application.

## Configuration

```yaml
newrelic:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  applicationIDs:
    - 10549735
    - 499785
  deployCount: 6
  enabled: true
  position:
    top: 4
    left: 3
    height: 1
    width: 2
  refreshInterval: 900
```

### Attributes

`apiKey` <br />
Value: Your <a href="https://docs.newrelic.com/docs/apis/getting-started/intro-apis/access-rest-api-keys">New Relic API</a> token.

`applicationIDs` <br />
The integer IDs of the New Relic applications you wish to report on. <br
/>
Values: A list of zero or more application IDs.

`deployCount` <br />
The number of past deploys to display on screen. <br />
Values: A positive integer, `0..n`.

`enabled` <br />
Determines whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

## Source Code

```bash
wtf/newrelic/
```
