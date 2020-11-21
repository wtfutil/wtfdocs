---
title: "Configuration"
date: 2018-04-15T21:17:16-07:00
draft: false
weight: 20
alwaysopen: false
---

# Configuration Files

By default WTF looks in a `~/.config/wtf/` directory for a YAML file called
`config.yml`. If the `~/.config/wtf/` directory doesn't exist, WTF will create that directory
on start-up, and then display instructions for creating a new
configuration file.

In other words, WTF expects to have a YAML config file at: `~/.config/wtf/config.yml`.

#### Example Configuration Files

A number of example configuration files are provided in the `_sample_configs/`
directory of the [Git repository](https://github.com/wtfutil/wtf/tree/master/_sample_configs).

To try out WTF quickly, copy
`sample_config.yml` into `~/.config/wtf/` as `config.yml` and relaunch WTF. You
should see the app launch and display the [Security](/modules/security),
[Clocks](modules/clocks/) and [Status](/modules/status/) widgets onscreen.

#### Custom Configuration Files

To try out different configurations (or run multiple instances of WTF),
you can pass the path to a config file via command line arguments on
start-up.

To load a custom configuration file (ie: one that's not
`~/.config/wtf/config.yml`), pass in the path to configuration file as a
parameter on launch:

```bash
❯ wtfutil --config=path/to/custom/config.yml
```
