---
title: What is the process for calculating the md5 sum of a string in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can get the MD5 sum of a string using Python by using the hashlib.md5() function.
---

**Contents**

[TOC]

# Section 1: Importing Libraries

In order to get the MD5 sum of a string, we need to import the `hashlib` library.

```python
import hashlib
```

# Section 2: Generating MD5 Hash

We then need to generate the MD5 hash of the string by using the `hashlib.md5()` function.

```python
string = "Hello World!"
md5_hash = hashlib.md5(string.encode())
```

# Section 3: Getting the MD5 Sum

After generating the MD5 hash, we can get the MD5 sum by using the `hexdigest()` function.

```python
md5_sum = md5_hash.hexdigest()
```

# Section 4: Output

Finally, we can print out the MD5 sum of the string.

```python
print(md5_sum)
# Output: 65a8e27d8879283831b664bd8b7f0ad4
```
