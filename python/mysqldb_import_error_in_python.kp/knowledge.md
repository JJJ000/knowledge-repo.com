---
title: There is no module installed that is called mysqldb
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: MySQLdb is not included in the standard Python library, so it must be installed separately.
---

**Contents**

[TOC]

# Solution

## Install Package

The easiest way to install the MySQLdb module is to install the package `mysqlclient`. This package can be installed using `pip` or `conda` depending on your Python distribution.

## Install from Source

If you are unable to install the `mysqlclient` package, you can install MySQLdb from source. To do this, you will need to download the source code from the [MySQLdb website](https://sourceforge.net/projects/mysql-python/files/mysql-python/1.2.3/). Once downloaded, extract the files and run the following command from the directory containing the source code:

```
python setup.py install
```

## Troubleshooting

If you are still unable to install the MySQLdb module, there may be an issue with the version of Python you are using. MySQLdb is only compatible with Python 2.x, so if you are using Python 3.x, you will need to install a compatible version of MySQLdb.
