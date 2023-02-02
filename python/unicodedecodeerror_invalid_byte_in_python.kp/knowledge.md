---
title: Error decoding unicode character invalid byte in the sequence
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A UnicodeDecodeError is raised when a byte sequence is encountered that is not valid for the specified encoding.
---

**Contents**

[TOC]

**What is a UnicodeDecodeError?**

A UnicodeDecodeError is an error that occurs when python is trying to decode a string of text that contains non-Unicode characters. This can happen when a file or string of text is encoded in a different character set than the one python is expecting.

**What is an Invalid Continuation Byte?**

An invalid continuation byte is a byte that is not part of the valid character set that is being used to decode the string of text. This can happen when a file or string of text is encoded in a different character set than the one python is expecting.

**What Causes a UnicodeDecodeError?**

A UnicodeDecodeError can be caused by a variety of things, such as an invalid byte sequence, an invalid character encoding, or an invalid byte order mark.

**How to Fix a UnicodeDecodeError?**

The best way to fix a UnicodeDecodeError is to figure out what the source of the problem is. This could mean checking the encoding of the file or string of text, as well as making sure the character set is set correctly. Once the source of the problem has been identified, it can then be fixed by applying the correct encoding.
