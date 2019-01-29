---
title: "Uninstall"
date: 2018-01-28T09:59:40-07:00
draft: false
---

## Remove the Binary and Configuration

`wtf` ships as a single binary. Assuming you have installed the binary, you can run:

```bash
rm $(which wtf)
```

If you have configured `wtf`, you will also want to delete your configs:

```bash
rm ~/.config/wtf
```

and that should also do it.
