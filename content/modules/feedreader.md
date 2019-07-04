---
title: "Feed Reader"
date: 2019-07-04T05:53:08-04:00
draft: false
weight: 65
---

<img class="screenshot" src="/imgs/modules/feedreader.png" width="320" height="94" alt="feedreader screenshot" />

A rudimentary RSS & Atom feed reader.

## Keyboard Commands

<span class="caption">Key:</span> `[return]` <br />
<span class="caption">Action:</span> Open the selected story in the browser.

<span class="caption">Key:</span> `j` <br />
<span class="caption">Action:</span> Select the next story in the list.

<span class="caption">Key:</span> `k` <br />
<span class="caption">Action:</span> Select the previous story in the list.

<span class="caption">Key:</span> `o` <br />
<span class="caption">Action:</span> Open the selected story in the browser.

<span class="caption">Key:</span> `r` <br />
<span class="caption">Action:</span> Refresh the data.

<span class="caption">Key:</span> `↓` <br />
<span class="caption">Action:</span> Select the next story in the list.

<span class="caption">Key:</span> `↑` <br />
<span class="caption">Action:</span> Select the previous story in the list.

## Configuration

```yaml
feedreader:
  enabled: true
  feeds:
  - https://news.ycombinator.com/rss
  - http://feeds.reuters.com/Reuters/worldNews
  feedLimit: 10
  position:
    top: 4
    left: 1
    height: 1
    width: 2
  refreshInterval: 14400
```

### Attributes

`enabled` <br />
Whether or not this module is executed and if its data displayed onscreen. <br />
Values: `true`, `false`.

`focusChar` <br />
Define one of the number keys as a short cut key to access the widget. <br />

`feedLimit` <br />
_Optional_ <br />
Defines number of stories from each feed to be displayed. Default is `-1`, which will display all available stories.<br />
Values: Any integer greater than zero. Values zero or less will display all.

`feeds` <br />
An array of RSS or Atom feed URLs.

`position` <br />
Defines where in the grid this module's widget will be displayed. <br />

`refreshInterval` <br />
How often, in seconds, this module will update its data. <br />
Values: A positive integer, `0..n`.

## Source Code

```bash
wtf/feedreader/
```