---
title: "Getting Started"
date: 2018-05-21T16:11:58-07:00
draft: false
weight: 10
alwaysopen: true
---

## Quick Start

`❯ brew install wtfultil`

or

1. <a href="https://github.com/wtfutil/wtf/releases">Download</a> the stand-alone, compiled binary.
2. Unzip the downloaded file.
3. From the command line, `cd` into the newly-created `/wtf` directory.
4. From the command line, run the app: `./wtfutil`

This should launch the app in your terminal using the default simple
configuration. See [Configuration](/configuration/files) for
more details.

See [Installation](/installation/) for additional installation options.

## Command-line Options

`--config, -c` <br />
Allows you to define a custom config file to use. See [Configuration](/configuration/files) for more details.

`--help, -h` <br />
Shows help information for the command-line arguments that WTF takes.

`--module, -m` <br />
Shows help information for the specific named module, if that module supports help text.

Example: `wtf --module=todo`.

`--version, -v` <br />
Shows version info.

## Keyboard Commands

<span class="caption">Key:</span> `Ctrl-R` <br />
<span class="caption">Action:</span> Force-refresh the data for all modules.

<span class="caption">Key:</span> `Esc` <br />
<span class="caption">Action:</span> Remove focus the currently-focused
widget.

<span class="caption">Key:</span> `Tab` <br />
<span class="caption">Action:</span> Move between focusable modules (`Shift-Tab` to move backwards).
