---
title: What is the proper method of defining the encoding of Python source code?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The correct way to define Python source code encoding is to use a special comment at the beginning of the file # -*- coding utf-8 -*-.
---

**Contents**

[TOC]

## Introduction

Python is one of the most popular programming languages for its simplicity, versatility, and efficiency. However, its simple syntax has its limitations when it comes to the representation of special characters and punctuation in various languages besides English. Therefore, Python introduced source code encoding as a way to facilitate the representation of different language characters in the source code of a program.

## Definition

Source code encoding is an instruction at the beginning of a Python source file that tells the interpreter which character encoding to use for interpreting the file's contents. The encoding is defined using an encoding declaration which might look like `# coding: <encoding name>` or `# -*- coding: <encoding name> -*-`. 

## Purpose

Source code encoding is essential for Python programmers dealing with non-ASCII characters like special letters, diacritics, or punctuation.  The proper encoding instruction in the header of the source code ensures that the Python interpreter can correctly understand and decode non-ASCII characters, allowing Python programs that work with various languages to execute without throwing decoding errors.

## Best practices

1. Unicode UTF-8 is the most common language encoding format for modern software development. Therefore, it is a good practice to set the default Python encoding to UTF-8 by entering `# -*- coding: utf-8 -*-` as the first line of the source code.
2. Follow the PEP-8 Python style guide recommendations for line length limit and interpretive comment styles.
3. Ensure that the chosen encoding is supported in Python itself and the operating system running it. 
4. Set the text editor or IDE program to save the file contents with the intended encoding.
5. Avoid using the Byte Order Mark (BOM) symbol as this might cause compatibility issues when running the code on different platforms.
