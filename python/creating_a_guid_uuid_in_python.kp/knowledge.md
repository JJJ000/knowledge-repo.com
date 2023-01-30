---
title: What is the process for generating a guid/uuid in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the uuid module`s uuid4() function to generate a random UUID in Python.
---

**Contents**

[TOC]

# Section 1: Introduction
A GUID (Globally Unique Identifier) or UUID (Universally Unique Identifier) is an identifier that is unique across both space and time. It is often used in software development to identify resources, such as database records, and ensure that they are not duplicated. In Python, there are several ways to generate a GUID/UUID.

# Section 2: Using the uuid Module
The uuid module in Python provides a number of functions for generating UUIDs. The most common function is uuid4(), which generates a random UUID. To generate a UUID using this function, simply import the uuid module and call the uuid4() function:

```python
import uuid

my_uuid = uuid.uuid4()
print(my_uuid)
```

# Section 3: Using the secrets Module
The secrets module in Python provides a secure way to generate random numbers for the purpose of generating UUIDs. To generate a UUID using this function, simply import the secrets module and call the token_hex() function:

```python
import secrets

my_uuid = secrets.token_hex()
print(my_uuid)
```

# Section 4: Using the OS Module
The os module in Python provides a number of functions for generating UUIDs. The most common function is urandom(), which generates a random UUID. To generate a UUID using this function, simply import the os module and call the urandom() function:

```python
import os

my_uuid = os.urandom(16)
print(my_uuid)
```
