---
title: "Installing With Homebrew"
date: 2019-07-12T07:27:20-07:00
draft: false
---

<small>{{ page.meta.date }}</small>

As of today WTF can be installed on macOS using [Homebrew](https://brew.sh):

```bash
brew tap wtfutil/wtfutil
brew install wtfutil

wtfutil
```

If everything goes according to plan, you should now find `wtfutil` on your system as an executable binary:

```bash
❯ which wtfutil
/usr/local/bin/wtfutil
```

```bash
❯ ls /usr/local/bin/wtfutil
lrwxr-xr-x  1 xxxxxx  admin  36 11 Jul 17:29 /usr/local/bin/wtfutil -> ../Cellar/wtfutil/0.16.1/bin/wtfutil
```