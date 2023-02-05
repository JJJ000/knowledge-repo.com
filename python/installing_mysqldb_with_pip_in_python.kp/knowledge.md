---
title: What is the process for installing the Python mysqldb module using pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Run `pip install mysqlclient` to install the Python MySQLdb module using pip.
---

**Contents**

[TOC]

## Installation

1. Install the Python pip package manager:
```
$ sudo apt-get install python-pip
```

2. Install the MySQLdb module:
```
$ pip install MySQL-python
```

## Verification

1. Verify that the module is installed correctly by importing it in Python:
```
$ python
>>> import MySQLdb
```

2. If the module is installed correctly, no errors should be returned.
