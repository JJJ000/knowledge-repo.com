---
title: An issue occurred while installing psycopg2 due to the inability to locate the -lssl library
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You need to install OpenSSL and its development packages before installing psycopg2 using the command `sudo apt-get install libssl-dev` on Ubuntu or `brew install openssl` on macOS.
---

**Contents**

[TOC]

Section 1: Introduction
Psycopg2 is a popular PostgreSQL database adapter used by Python developers. When installing psycopg2, it's not uncommon to run into an error that says "library not found for -lssl." This error occurs because psycopg2 needs the OpenSSL libraries to be installed on your system, and they aren't available.

Section 2: Solution
To resolve the "library not found for -lssl" error when installing psycopg2, you need to install the OpenSSL libraries on your system. Here are the steps to follow:

1. Open a Terminal window on your system.
2. Type the following command to install OpenSSL: sudo apt-get install libssl-dev
3. Enter your system password when prompted.
4. Wait for the installation to complete.
5. After the installation has completed, try installing psycopg2 again using pip.

Section 3: Alternative Solutions
If the above solution doesn't work, here are some alternative solutions you can try:

1. If you're on a Mac, you can use Homebrew to install OpenSSL: brew install openssl
2. If you're on Windows, you can download the OpenSSL libraries from the OpenSSL website and install them manually.
3. You can also try installing psycopg2-binary instead of psycopg2, as it includes all the necessary dependencies and may not require the OpenSSL libraries.

Section 4: Conclusion
In conclusion, the "library not found for -lssl" error when installing psycopg2 is caused by a missing dependency – the OpenSSL libraries. By installing the OpenSSL libraries on your system, you can resolve this error and continue using psycopg2 to interact with your PostgreSQL databases.
