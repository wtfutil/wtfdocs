---
title: "Creating New Modules"
date: 2019-04-28
draft: false
weight: 30
---

The [widgets](../glossary/#widget) that you see on the screen are displayed using [modules](../glossary/#module). To make it easier to create new modules there is a generator which creates a stub (an empty module). The Go package _generators_ contains generator scripts for different types of widgets.

## Prerequisites

Before you can generate new modules, you'll need to have:

* Go version 1.11 or higher
* The source code of WTF (`git clone https://github.com/wtfutil/wtf`)

## New TextWidgets

You can run `go generate -run=text` to create a new widget called **NewTextWidget**. You can change the name of the generated widget by setting an environment variable called `WTF_WIDGET_NAME`.

For example, to generate a new widget called _MySuperAwesomeWidget_ on macOs or linux, the command would be:

{{< code lang="bash" >}}
# as a single line
WTF_WIDGET_NAME=MySuperAwesomeWidget go generate -run=text
# setting the name separately
export WTF_WIDGET_NAME=MySuperAwesomeWidget
go generate -run=text
```

The equivalent using Windows PowerShell would be

{{< code lang="powershell" >}}
$env:WTF_WIDGET_NAME = "MySuperAwesomeWidget"
go generate -run=text
```

The new widget is generated using the template in `textwidget.tpl`

## Source Code

{{< code lang="bash" >}}
wtf/generator/
```