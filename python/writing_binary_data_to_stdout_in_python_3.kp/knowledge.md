---
title: What is the process of writing binary data to stdout using Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `sys.stdout.buffer.write()` method to write binary data to stdout in Python 3.
---

**Contents**

[TOC]

## Introduction

Writing binary data to stdout in Python 3 can be accomplished using the appropriate encoding. In this tutorial, we will explore how to write binary data to stdout in Python 3 through four sections.

## Section 1: sys.stdout.buffer

The `sys.stdout.buffer` attribute provides a binary write mode for output to stdout.

```python
import sys

sys.stdout.buffer.write(b"binary data")
```

In the example above, `sys.stdout.buffer.write()` is used to write binary data to stdout.

## Section 2: io.BytesIO

`io.BytesIO` is a class that allows us to write to an in-memory buffer object as if it were a binary file.

```python
import io

stdout_buffer = io.BytesIO()
stdout_buffer.write(b"binary data")
sys.stdout.buffer.write(stdout_buffer.getvalue())
```

In the example above, `io.BytesIO()` creates an in-memory buffer object, and `stdout_buffer.write()` is used to write binary data to it. Later, the `sys.stdout.buffer.write()` method is used to write to stdout using the `stdout_buffer.getvalue()` method.

## Section 3: Encode binary data with base64

Another way to write binary data to stdout is to encode it using the base64 module.

```python
import base64

binary_data = b"binary data"
encoded_data = base64.b64encode(binary_data)
sys.stdout.write(encoded_data.decode('utf-8'))
```

In the example above, `base64.b64encode()` is used to encode the binary data into base64 format. The `sys.stdout.write()` method is used to write the encoded data to stdout.

## Section 4: Using the print function

The print function can be used to write binary data to stdout through string formatting.

```python
binary_data = b"binary data"
print(binary_data.decode('utf-8', 'backslashreplace'), end='', flush=True)
```

In the example above, `print()` is used to write binary data to stdout through string formatting. The `end=''` parameter ensures that there is no newline character added to the end of the print statement. The `flush=True` parameter ensures that the output is flushed immediately without buffering. 

## Conclusion 

Writing binary data to stdout in Python 3 is a relatively easy task. We hope this tutorial has been helpful in demonstrating four different ways to accomplish this task.
