---
title: "Binary Renamed to 'wtfutil'"
date: 2019-07-10T10:09:34-07:00
draft: false
---

<small>{{ page.meta.date }}</small>

With the release of [v0.15.0](https://github.com/wtfutil/wtf/releases/tag/v0.15.0), the installed binary has been renamed from `wtf` to `wtfutil`.

To execute it, you must now use:

```bash
wtfutil
```

The name has changed because calling it `wtf` caused a collision with the venerable and amusing [bsd-wtf](https://sourceforge.net/projects/bsdwtf/) utility. This wasn't a problem back when there was only one person using WTF and no one else knew about it, but with the rise in popularity this collision has been causing problems for some people.

Given that `bsd-wtf` was created long before WTF, it only seems proper to abdicate the name.

(And if you want to check out the original `wtf`, it's available via [Homebrew](https://formulae.brew.sh/formula/wtf) on macOS, and presumably via `apt-get` on Linux).