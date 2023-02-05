---
title: What is the purpose of using 'b' when encoding a string with base64?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Base64 encoding requires the use of `b` to indicate that the data being encoded is in binary format.
---

**Contents**

[TOC]

# Overview

Base64 is an encoding scheme used to represent binary data in an ASCII string format. It is commonly used in email and other web applications to encode binary data such as images, audio, and video. In Python, the ‘b’ character is used to indicate that the data being encoded is binary data, rather than text data.

# Base64 Encoding

Base64 encoding is a process of converting binary data into a string of characters that can be represented in an ASCII format. The encoded string consists of only printable characters, such as uppercase and lowercase letters, numbers, and a few special characters. The output of the encoding process is a string of characters that can be used to represent the original binary data.

# Python

In Python, the ‘b’ character is used to indicate that the data being encoded is binary data, rather than text data. This is necessary because the base64 encoding algorithm only works with binary data. If the data is not binary, it will not be encoded correctly. Without the ‘b’ character, the encoding process will not work properly.

# Conclusion

In summary, the ‘b’ character is used to indicate that the data being encoded is binary data in Python. Without this character, the base64 encoding algorithm will not work properly and the data will not be encoded correctly.
