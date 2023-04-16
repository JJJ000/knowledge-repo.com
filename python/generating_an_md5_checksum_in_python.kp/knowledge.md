---
title: Creating an md5 hash of a file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, an MD5 checksum of a file can be generated using the hashlib library`s md5() function.
---

**Contents**

[TOC]

# Using the hashlib Module

The `hashlib` module in Python allows users to generate an MD5 checksum of a file. The following steps can be used to generate an MD5 checksum of a file:

1. Import the `hashlib` module:

```python
import hashlib
```

2. Open the file in binary read mode:

```python
f = open('filename', 'rb')
```

3. Create a hash object:

```python
m = hashlib.md5()
```

4. Read the file content in chunks and update the hash object:

```python
while True:
    data = f.read(1024)
    if not data:
        break
    m.update(data)
```

5. Get the MD5 checksum:

```python
checksum = m.hexdigest()
```

# Using the md5sum Command

On Linux systems, the `md5sum` command can be used to generate an MD5 checksum of a file. The following steps can be used to generate an MD5 checksum of a file:

1. Open a terminal window.

2. Change the current directory to the directory containing the file.

3. Run the following command:

```bash
md5sum filename
```

4. The output of the command will be the MD5 checksum of the file.
