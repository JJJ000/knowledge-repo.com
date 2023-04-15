---
title: Attempting to install the mysql-python package via pip fails with an environmenterror due to mysql_config not being found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: MySQL-python requires the MySQL C API development headers and libraries to be installed on your machine.
---

**Contents**

[TOC]

# Solution 1:

## Install MySQL Client Library

The first step is to install the MySQL client library, which contains the mysql_config tool. Depending on the operating system, this can be done in different ways.

For Ubuntu/Debian:

```
sudo apt-get install libmysqlclient-dev
```

For RedHat/CentOS:

```
sudo yum install mysql-devel
```

For Mac OS X:

```
brew install mysql-connector-c
```

## Install MySQL-Python

Once the client library is installed, the MySQL-Python package can be installed using pip:

```
pip install mysql-python
```

# Solution 2:

## Download MySQL-Python

If the above steps do not work, the MySQL-Python package can be downloaded from the official website and installed manually.

## Install MySQL-Python

Once the package is downloaded, it can be installed using the following command:

```
python setup.py install
```
