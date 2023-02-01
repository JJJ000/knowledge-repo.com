---
title: The mysql_config file could not be located when attempting to install the mysqldb Python interface
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: MySQLdb requires the `mysql\_config` executable to be installed and available on the PATH.
---

**Contents**

[TOC]

**Solution 1:**

Using apt-get

1. Install the `libmysqlclient-dev` package:
   ```
   sudo apt-get install libmysqlclient-dev
   ```
2. Install the Python MySQLdb module:
   ```
   pip install MySQL-python
   ```

**Solution 2:**

Using yum

1. Install the `mysql-devel` package:
   ```
   sudo yum install mysql-devel
   ```
2. Install the Python MySQLdb module:
   ```
   pip install MySQL-python
   ```
