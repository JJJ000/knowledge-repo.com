---
title: What is the distinction between sys.stdout.write and print?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Sys.stdout.write does not add a new line at the end of the output, whereas print does.
---

**Contents**

[TOC]

1. Syntax

- **sys.stdout.write**: sys.stdout.write(string)
- **print**: print(string)

2. Output

- **sys.stdout.write**: Writes the given string to the standard output stream without adding a new line character at the end.
- **print**: Writes the given string to the standard output stream and adds a new line character at the end.

3. Return Value

- **sys.stdout.write**: Returns the number of characters written to the stream.
- **print**: Returns None.

4. Usage

- **sys.stdout.write**: Used for writing to the standard output stream without adding a new line character at the end.
- **print**: Used for writing to the standard output stream with a new line character at the end.
