---
title: "Creating New Modules"
date: 2021-12-12
draft: false
weight: 30
---

# Creating New Modules

The [widgets](../glossary/#widget) that you see on the screen are displayed using [modules](../glossary/#module). To make it easier to create new modules there is a generator which creates a stub (an empty module). The Go package _generators_ contains generator scripts for different types of widgets.

## Prerequisites

Before you can generate new modules, you'll need to have:

* Go version 1.15 or higher
* The source code for WTF (`git clone https://github.com/wtfutil/wtf`)

## Creating a New Text Widget

1. Generate a new module using generator  
   Use `go run generator/textwidget.go` to create a new widget called **NewTextWidget**. You can change the name of the generated widget by setting an environment variable called `WTF_WIDGET_NAME`.

    For example, to generate a new widget called _MyNewWidget_ on macOs or linux, the command would be:
    
    ```bash
    # as a single line
    ❯ WTF_WIDGET_NAME=MyNewWidget go run generator/textwidget.go
    
    # setting the name separately
    ❯ export WTF_WIDGET_NAME=MyNewWidget
    ❯ go run generator/textwidget.go
    ```
    
    The equivalent using Windows PowerShell would be
    
    ```bash
    ❯ $env:WTF_WIDGET_NAME = "MyNewWidget"
    ❯ go run generator\textwidget.go 
    ```

    The new widget is generated using the template in `textwidget.tpl`

2. Register your newly generated module in app  

   The last step is to register your new module in `app/widget_maker.go`, you will have to import your module and define a new case with your module name.


3. Run you app, your module should be present !


## Source Code

```bash
wtf/generator/
```
