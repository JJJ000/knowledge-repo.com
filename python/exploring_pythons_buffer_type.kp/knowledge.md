---
title: What purpose does the Python 'buffer' type serve?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Python `buffer` type is used for efficient access to data stored in memory.
---

**Contents**

[TOC]

# Python Buffer Type

Python provides a `buffer` type to create a mutable buffer object, which can store raw bytes of data. This buffer object can be used to access and manipulate a contiguous block of memory.

## Creation of Buffer Object

A buffer object can be created by passing a source object to `buffer` constructor, which can be a string, bytearray, memoryview or another buffer object.

```python
data = bytearray(b'Hello World!')
buf = buffer(data)
```

## Accessing and Manipulating Buffer Object

Once a buffer object is created, it can be used to access and manipulate the source data using the standard indexing and slicing operations.

```python
print buf[0]                                      # 72
print buf[1:5]                                    # <read-only buffer for ... at 0x000002683719CEE8>
buf[6:11] = b'world'                              # Changes buffer content to b'Hello world!'
```

## Buffer Protocol

Buffer object follows the Python buffer protocol, which defines an interface to export a contiguous block of memory to other C extension modules, without copying the data.

The buffer protocol provides two methods- `getbuffer()` and `releasebuffer()` to export and release the buffer respectively.

```python
class MyBuffer:
    def __init__(self, length):
        self.buf = bytearray(length)

    def getbuffer(self, flags):
        return buffer(self.buf)

    def releasebuffer(self, buffer):
        pass  # Optional
```

## Conclusion

The `buffer` type in Python is useful when working with large amounts of binary data. It provides a convenient way to access and manipulate the memory blocks in a fast and efficient way, as well as allowing for easy integration with other C extensions through the buffer protocol.
