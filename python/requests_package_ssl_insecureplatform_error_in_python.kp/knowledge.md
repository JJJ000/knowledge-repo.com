---
title: When utilizing the requests package, encountering the ssl insecureplatform error
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The SSL InsecurePlatform error occurs when using an outdated version of Python that does not support modern SSL protocols.
---

**Contents**

[TOC]

Overview
--------

When using the `requests` package in Python, you may encounter an `InsecurePlatform` error if you have an outdated version of `OpenSSL` installed on your machine. This error occurs because `requests` uses `OpenSSL` to handle SSL (Secure Sockets Layer) certificate validation, and some versions of `OpenSSL` are no longer considered secure.



Solution
--------

To solve this problem, you need to update your version of `OpenSSL`. However, this can be challenging on some platforms, such as Windows, where `OpenSSL` is not installed by default. One solution is to install a pre-built version of `OpenSSL` using a package manager, such as `conda` (for Anaconda) or `brew` (for Homebrew on macOS). 

Alternatively, you can try upgrading your version of `requests` to a more recent version. Newer versions of `requests` include a fallback option that does not require `OpenSSL` to be updated.

Update OpenSSL
--------------

Follow the instructions below to update `OpenSSL`:

### Step 1: Verify your OpenSSL version

To find out your current version of `OpenSSL`, run the following command in your terminal:

```bash
openssl version
```

This will display the current version of `OpenSSL`. If you have an outdated version, you will need to update it.


### Step 2: Identify your platform

The steps to update `OpenSSL` will depend on your platform. There are different methods for macOS, Linux, and Windows.


### Step 3: Install a pre-built OpenSSL package

Some package managers, such as `conda` and `brew`, offer pre-built versions of `OpenSSL` that you can install with a single command. 

#### Conda

If you are using Anaconda, you can update `OpenSSL` with the following command:

```bash
conda install openssl
```

#### Brew

If you are using Homebrew on macOS, you can update `OpenSSL` with the following command:

```bash
brew install openssl
```

### Step 4: Verify the new OpenSSL version

After installing the new version of `OpenSSL`, you should verify it by running the `openssl version` command again. This should display the updated version number.


Update requests
---------------

Alternatively, you can try upgrading your version of `requests` to a more recent version that includes a fallback option that does not require `OpenSSL` to be updated. To upgrade `requests`, run the following command:

```bash
pip install requests --upgrade
```

This will install the latest version of `requests`. After upgrading, try running your code again to see if the error has been resolved.


Conclusion
----------

In summary, the `InsecurePlatform` error when using the `requests` package in Python is caused by an outdated version of `OpenSSL`. To solve this problem, you can update your version of `OpenSSL` or upgrade to a newer version of `requests`. With these solutions, you should be able to handle SSL certificate validation successfully.
