---
title: There is an error when trying to import the configparser module in Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The ConfigParser module is not available in Python 3, so it must be imported from the backported configparser module.
---

**Contents**

[TOC]

# Solution

## Install ConfigParser
ConfigParser is a Python module that can be used to read and write configuration files. To install ConfigParser, run the following command in your terminal:

`pip install configparser`

## Import ConfigParser
After installing ConfigParser, you can import it in your Python script using the following statement:

`import ConfigParser`

## Use ConfigParser
Once imported, you can use ConfigParser to read and write configuration files. For example, to read a configuration file named "config.ini", you can use the following code:

```
config = ConfigParser.ConfigParser()
config.read('config.ini')
```

## Troubleshooting
If you are still getting an ImportError, make sure that you are using the correct spelling and case for the module name (i.e. ConfigParser, not configparser). Additionally, make sure that the module is installed in the correct Python environment.
