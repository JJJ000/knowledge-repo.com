---
title: How do I convert bytes to a hexadecimal string in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The correct way to convert bytes to a hex string in Python 3 is to use the hex() function.
---

**Contents**

[TOC]

**Using binascii.hexlify()**

1. Import the binascii library:

```python
import binascii
```

2. Pass the bytes object to the hexlify() function:

```python
hex_string = binascii.hexlify(b'Hello World!')
```

3. Print the hex string:

```python
print(hex_string)
# b'48656c6c6f20576f726c6421'
```

**Using the bytes.hex() Method**

1. Create a bytes object:

```python
byte_string = b'Hello World!'
```

2. Pass the bytes object to the hex() method:

```python
hex_string = byte_string.hex()
```

3. Print the hex string:

```python
print(hex_string)
# 48656c6c6f20576f726c6421
```
