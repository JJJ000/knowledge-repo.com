---
title: What location does pip use to install its packages?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: By default, pip installs packages to the Python installation`s site-packages directory.
---

**Contents**

[TOC]

## Default Location
By default, pip installs packages to the `site-packages` directory of the active Python installation. This location is typically in the following path:

`C:\Python27\Lib\site-packages`

## Alternate Locations
Users can also specify an alternate installation location by using the `--target` option with the `pip install` command.

## User Packages
If the `--user` option is specified with the `pip install` command, pip will install the package to the user's home directory. This location is typically in the following path:

`C:\Users\[username]\AppData\Roaming\Python\Python27\site-packages`
