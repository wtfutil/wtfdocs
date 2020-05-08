---
title: "Uninstallation"
date: 2018-01-28T09:59:40-07:00
draft: false
weight: 10
---

## Homebrew

{{< code lang="bash" >}}
brew uninstall wtfutil
```

## Remove the Binary and Configuration

WTF ships as a single binary named `wtfutil`. Assuming you have installed the binary, run:

{{< code lang="bash" >}}
rm $(which wtfutil)
```

If you have configured WTF, you will also want to delete your configs:

{{< code lang="bash" >}}
rm ~/.config/wtf
```

and that should also do it.
