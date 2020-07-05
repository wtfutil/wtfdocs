---
title: "Installation"
date: 2018-05-18T09:59:40-07:00
draft: false
weight: 1
---

## Homebrew

{{< code lang="bash" >}}
❯ brew tap wtfutil/wtfutil
❯ brew install wtfutil

❯ wtfutil
{{< /code >}}

## As a Binary

Grab the latest version from the <a href="https://github.com/wtfutil/wtf/releases">Releases page</a>.

Expand it, and `cd` into the resulting directory. Then run:

{{< code lang="bash" >}}
❯ ./wtfutil
{{< /code >}}

and that should also do it.

## From Source

Download the source code repo and install the dependencies:

{{< code lang="bash" >}}
# Set the Go proxy variable to GoCenter
❯ export GOPROXY="https://gocenter.io"

# Enable Go modules
❯ export GO111MODULE=on

❯ go get -u github.com/wtfutil/wtf
❯ cd $GOPATH/src/github.com/wtfutil/wtf
❯ make install
❯ make run
{{< /code >}}

and that should do it.

