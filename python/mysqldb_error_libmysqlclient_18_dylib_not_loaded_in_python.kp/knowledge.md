---
title: The library libmysqlclient.18.dylib was not loaded in python's mysqldb
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The issue is likely caused by a missing or outdated version of the libmysqlclient library that the Python MySQLdb module is dependent on.
---

**Contents**

[TOC]

Overview
--------
If you are encountering an issue of `Library not loaded: libmysqlclient.18.dylib` while using MySQLdb module in Python, it is most likely that the `libmysqlclient` shared library is either not installed or the system is not able to locate it. This error usually occurs in macOS environments where MySQL is not installed through Homebrew. In this guide, we will learn about the possible solutions to fix the "Library not loaded: libmysqlclient.18.dylib" error.


Install MySQL Client Library
---------------------------
The first solution to fix the "Library not loaded: libmysqlclient.18.dylib" error is to install the MySQL client library on your system. You can either download and install the library from the MySQL website or through package managers like Homebrew. Here is how you can install the library through Homebrew:

1. Open the Terminal app on your macOS system.
2. Install Homebrew if not already installed by running the following command in the Terminal:
    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
3. Once Homebrew is installed, install the MySQL client library by running the following command:
    ```
    brew install mysql-connector-c
    ```
4. After the installation is completed, verify the library is installed correctly by running the following command:
    ```
    ls /usr/local/lib/libmysqlclient*
    ```
    You should see the `libmysqlclient.18.dylib` file listed.


Update DYLD_LIBRARY_PATH Environment Variable
----------------------------------------------
If installing the MySQL client library does not fix the issue, you can try updating the `DYLD_LIBRARY_PATH` environment variable to include the path where the `libmysqlclient` shared library is located. Here is how you can update the `DYLD_LIBRARY_PATH` environment variable:

1. Open the Terminal app on your macOS system.
2. Run the following command to open the `.bash_profile` file:
    ```
    open -e ~/.bash_profile
    ```
3. Add the following line to the file:
    ```
    export DYLD_LIBRARY_PATH="/usr/local/mysql/lib:$DYLD_LIBRARY_PATH"
    ```
4. Save and close the file.
5. Reload the environment variables by running the following command:
    ```
    source ~/.bash_profile
    ```


Update LD_LIBRARY_PATH Environment Variable
--------------------------------------------
If you are using a Linux system, the `Library not loaded: libmysqlclient.18.dylib` error can be fixed by updating the `LD_LIBRARY_PATH` environment variable. Here is how you can update the `LD_LIBRARY_PATH` environment variable:

1. Open the Terminal app on your Linux system.
2. Run the following command to open the `.bashrc` file:
    ```
    nano ~/.bashrc
    ```
3. Add the following line to the file:
    ```
    export LD_LIBRARY_PATH="/usr/local/mysql/lib:$LD_LIBRARY_PATH"
    ```
4. Save and close the file.
5. Reload the environment variables by running the following command:
    ```
    source ~/.bashrc
    ```


Conclusion
----------
In this guide, we have learned about the possible solutions to fix the "Library not loaded: libmysqlclient.18.dylib" error while using the MySQLdb module in Python. The solutions include installing the MySQL client library, updating the `DYLD_LIBRARY_PATH` environment variable for macOS systems, and updating the `LD_LIBRARY_PATH` environment variable for Linux systems.
