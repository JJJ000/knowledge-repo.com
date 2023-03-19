---
title: Python code to save file as utf-8?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To write to a UTF-8 encoded file in Python, include the encoding parameter when opening the file with the `w` or `a` mode.
---

**Contents**

[TOC]

# Introduction

In this tutorial, we will learn how to write to a UTF-8 encoded file in Python.

# Step 1: Open file in write mode with UTF-8 encoding

To write to a file in UTF-8 encoding, we need to open the file in write mode with UTF-8 encoding. We can do this using the `open()` function with the `'w'` mode and specifying the `'utf-8'` encoding.

Here's an example:

```
with open('utf8file.txt', mode='w', encoding='utf-8') as file:
    file.write('Hello, World! 😃\n')
```

In the above example, we opened the file `utf8file.txt` in write mode with UTF-8 encoding using the `with` statement. We then wrote the string `'Hello, World! 😃\n'` to the file using the `write()` method.

# Step 2: Writing strings with non-ASCII characters

If we want to write strings with non-ASCII characters to the file, we need to make sure that the characters are encoded properly in UTF-8 format.

Here's an example:

```
with open('utf8file.txt', mode='w', encoding='utf-8') as file:
    file.write('안녕하세요, 세계! 😃\n')
```

In the above example, we wrote the string `'안녕하세요, 세계! 😃\n'` to the file, which includes Korean characters and an emoji. These characters are automatically encoded in UTF-8 format because we opened the file in UTF-8 encoding.

# Step 3: Writing bytes to a UTF-8 file

In some cases, we may want to write binary data to a file in UTF-8 encoding. To do this, we need to convert the binary data to a UTF-8 encoded byte string before writing it to the file.

Here's an example:

```
data = b'\x48\x65\x6c\x6c\x6f\x2c\x20\xe4\xb8\x96\xe7\xb4\x80!\xf0\x9f\x98\x83\n'
with open('utf8file.txt', mode='wb') as file:
    file.write(data)
```

In the above example, we created a binary data string `data`, which includes both ASCII and non-ASCII characters. We then opened the file `utf8file.txt` in write mode with binary encoding (`'wb'`) and wrote the `data` string to the file using the `write()` method.

# Conclusion

In this tutorial, we learned how to write to a UTF-8 encoded file in Python by opening the file in write mode with UTF-8 encoding, writing strings with non-ASCII characters, and writing bytes to a UTF-8 file.
