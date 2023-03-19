---
title: Encountered an error of 'curl-config not found [errno 2] no such file or directory' while trying to install pycurl
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The error message suggests that curl-devel package is missing and needs to be installed before installing pycurl.
---

**Contents**

[TOC]

### Introduction
When installing pycurl in Python, you may come across the error message "Could not run curl-config: [Errno 2] No such file or directory". This error occurs because pycurl requires the curl development package to be installed on your system. In this article, we will discuss the steps you need to take to fix this error.

### Install Curl Development Package
The first step to fixing the "Could not run curl-config" error is to install the curl development package using the appropriate command for your system. For example, on Ubuntu or Debian-based systems, you can run the following command:

```
sudo apt-get install libcurl4-openssl-dev
```

On Red Hat-based systems, you can use the following command:

```
sudo yum install curl-devel
```

### Set Path to curl-config
After installing the curl development package, you need to set the path to the curl-config file. This file is used by pycurl to find the necessary libraries and include files. You can set the path by running the following command:

```
export PATH=$PATH:/usr/local/bin/
```

This command adds the /usr/local/bin/ directory to your PATH environment variable. If your curl-config file is located in a different directory, you should replace /usr/local/bin/ with the correct path.

### Reinstall Pycurl
Once you have installed the curl development package and set the path to the curl-config file, you should be able to install pycurl without encountering the "Could not run curl-config" error. You can reinstall pycurl using pip by running the following command:

```
pip install --no-cache-dir pycurl
```

The --no-cache-dir option is used to prevent pip from using any cached files during the installation process.

### Conclusion
In this article, we have discussed the steps you need to take to fix the "Could not run curl-config" error when installing pycurl in Python. By installing the curl development package, setting the path to the curl-config file, and reinstalling pycurl, you should be able to install and use pycurl without any issues.
