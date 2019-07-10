---
title: "Installation"
date: 2018-05-18T09:59:40-07:00
draft: false
weight: 1
---

## As a Binary

Grab the latest version from here:

```bash
https://github.com/wtfutil/wtf/releases
```

expand it, and `cd` into the resulting directory. Then run:

```bash
./wtfutil
```

and that should also do it.

## From Source

Download the source code repo and install the dependencies:

```bash
# Set the Go proxy variable to GoCenter
export GOPROXY="https://gocenter.io"

# Enable Go modules
export GO111MODULE=on

go get -u github.com/wtfutil/wtf
cd $GOPATH/src/github.com/wtfutil/wtf
make install
make run
```
and that should do it.

