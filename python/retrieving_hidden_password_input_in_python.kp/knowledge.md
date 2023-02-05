---
title: Retrieving a secret password entry
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the getpass() function from the getpass module.
---

**Contents**

[TOC]

# Using getpass Library
The getpass library can be used to get hidden password input from the user in Python. 

## Steps to use getpass
1. Import the getpass library.
```python
import getpass
```
2. Use the `getpass()` function to get the password input from the user.
```python
password = getpass.getpass("Enter your password: ")
```
3. Store the password in a variable.
```python
pwd = password
```
4. Use the stored password as required.
```python
print("Your password is:", pwd)
```
