---
title: Pip has been set up to access locations which require tls/ssl, but the ssl module in Python cannot be used
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The ssl module must be installed in order for pip to be able to connect to locations that require TLS/SSL.
---

**Contents**

[TOC]

## Solution 1: Install OpenSSL
1. Download the latest version of OpenSSL from [here](https://www.openssl.org/source/).
2. Follow the installation instructions for your operating system.
3. Once OpenSSL is installed, you should be able to use pip with locations that require TLS/SSL.

## Solution 2: Use a Different Python Version
1. Download and install the latest version of Python from [here](https://www.python.org/downloads/).
2. Make sure that the version of Python you are using includes the ssl module.
3. Once you have the correct version of Python installed, you should be able to use pip with locations that require TLS/SSL.
