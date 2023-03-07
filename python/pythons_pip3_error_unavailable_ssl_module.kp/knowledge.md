---
title: The Python package installation through pip3 fails because the ssl module is not accessible
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The error indicates that the SSL support is missing in the Python installation.
---

**Contents**

[TOC]

Possible answer:

Problem description: 

When trying to install a package with `pip3`, the following error message appears: "ssl module in Python is not available". 

Solution:

1. Install the required dependencies: 

The `ssl` module is part of the Python standard library and should be available in most Python installations. However, if it is missing, it may be necessary to install the OpenSSL development package and related dependencies in the OS. For example, in Debian-based systems, run the following command as root or with sudo: 

```
apt-get install libssl-dev
```

On Windows, it may be necessary to download and install the OpenSSL binaries manually. 

2. Reinstall Python with SSL support 

If the above step does not fix the issue, it may be necessary to reinstall Python with SSL support enabled. This involves recompiling Python from source with the `--with-ssl` flag enabled. Instructions for doing this vary depending on the OS and Python version, so consult the relevant documentation for more details. 

3. Use a different Python distribution 

If neither of the above steps work, it may be necessary to switch to a different Python distribution that includes SSL support by default. For example, the Anaconda distribution provides a pre-configured Python environment with SSL support and many popular packages already installed. 

4. Use a virtual environment 

If switching to a different Python distribution is not an option, or if the package needs to be installed in a specific Python version or virtual environment, it may be possible to create a virtual environment with SSL support enabled. One way to do this is to use the `pyenv` tool, which allows creating and managing multiple Python installations and switching between them easily. The `pyenv` installation instructions and usage are available at https://github.com/pyenv/pyenv. To enable SSL support when creating a new virtual environment, use the `--with-openssl` flag, like this: 

```
pyenv virtualenv --with-openssl 3.9.6 myenv
```

This will create a new Python 3.9.6 virtual environment named "myenv" with SSL support enabled. 

Note: depending on the specific OS, Python version, and other factors, some of these steps may not be necessary or may require additional configuration beyond the scope of this answer. In any case, it is recommended to consult the relevant documentation and/or seek help from experienced users or support forums.
