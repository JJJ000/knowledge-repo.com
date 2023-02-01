---
title: Pandas and Python are unable to decode a csv file resulting in a unicodedecodeerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Pandas can be used to specify an encoding when reading the CSV file to avoid a UnicodeDecodeError.
---

**Contents**

[TOC]

## What is a UnicodeDecodeError?
A UnicodeDecodeError is an error raised when a given sequence of bytes cannot be decoded into a Unicode string. It happens when the encoding of the file being read is not the same as the encoding of the system's default encoding.

## Why Does it Happen when Reading CSV Files?
CSV files are usually encoded in either ASCII or UTF-8, but the system's default encoding may not be the same. This can cause a UnicodeDecodeError when trying to read the file in Pandas with Python.

## How to Fix the Error
The best way to fix the error is to specify the encoding of the file when reading it in with Pandas. This can be done by adding the `encoding` parameter to the `read_csv()` function. For example, if the file is encoded in UTF-8, the following code can be used to read it in:

```
df = pd.read_csv('file.csv', encoding='utf-8')
```
