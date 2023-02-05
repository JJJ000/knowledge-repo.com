---
title: The 'utf8' codec is unable to interpret the byte 0x9c
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The `utf8` codec cannot decode bytes that are not valid utf8 characters.
---

**Contents**

[TOC]

# Overview

The `UnicodeDecodeError` occurs when a Unicode-based program attempts to decode a string of bytes that cannot be represented in the Unicode character set. In Python, this error is typically raised when a program attempts to decode a string of bytes using the 'utf8' codec, which is not able to decode the byte 0x9c.

# Causes

This error is typically caused by attempting to decode a string of bytes using the wrong encoding. The 'utf8' codec is only able to decode strings of bytes encoded using the UTF-8 character set, which does not include the byte 0x9c.

# Solutions

The best way to resolve this error is to determine the correct encoding of the string of bytes and decode it using the appropriate codec. If the encoding of the string is unknown, it may be possible to guess the encoding by examining the byte sequence and attempting to decode it with a variety of codecs. If this is not possible, it may be necessary to manually determine the correct encoding.
