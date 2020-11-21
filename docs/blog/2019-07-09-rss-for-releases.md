---
title: "Using WTF's FeedReader to Track WTF Releases"
date: 2019-07-09T17:07:58-07:00
description: "Cats and dogs"
draft: false
---

<small>{{ page.meta.date }}</small>

With the release of [v0.14.0](https://github.com/wtfutil/wtf/releases/tag/v0.14.0), WTF has the ability to track and display RSS and Atom feeds via the [FeedReader module](/modules/feedreader/).

And if you're reading this, you know that [wtfutil.com](https://wtfutil.com) now has a blog, and that blog is available via RSS at [https://wtfutil.com/blog/index.xml](https://wtfutil.com/blog/index.xml).

Putting the two together, you now have a great way to keep up-to-date on the most recent WTF releases, because all of them will be announced, with changlog details, on this very blog.

To configure WTF to do so, add the following `feedreader` configuration to your `config.yml` file:

```bash
feedreader:
  enabled: true
  feeds:
  - https://wtfutil.com/blog/index.xml
  feedLimit: 10
  position:
    top: 2
    left: 1
    width: 2
    height: 1
  updateInterval: 14400
```

Modify the `position` values accordingly for where you want it to appear onscreen.

`feedLimit` limits the number of stories displayed for any given feed. Without a feed limit, FeedReader will display all the stories returned by the feed.

I've set `updateInterval` to a fairly reasonable 14,400 seconds, or four hours, because most RSS content doesn't change that often.