---
title: Retrieve the md5 hash of large files using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Open the file in binary mode, read it into chunks, and use the hashlib library in a loop to update and digest the hash.
---

**Contents**

[TOC]

## Importing hashlib

To get the MD5 hash of big files in Python, we need to use the hashlib library. The hashlib library provides various cryptographic hash functions, including MD5. We can import the hashlib library using the following code:

```python
import hashlib
```

## Reading the file in chunks

If we try to read the entire content of a big file into memory at once, it can lead to memory errors. Therefore, we need to read the file in small chunks using a loop. We can define the chunk size as per our requirement. Generally, a chunk size of 4096 bytes is used. We can use the following code to read the file in chunks:

```python
def get_file_md5(filename):
    hash_md5 = hashlib.md5()
    with open(filename, "rb") as f:
        while True:
            chunk = f.read(4096)
            if not chunk:
                break
            hash_md5.update(chunk)
    return hash_md5.hexdigest()
```

In the above code, we first initialize an MD5 hash object using the hashlib.md5() function. Then, we open the file in binary mode using the open() function and read it in chunks of 4096 bytes using the read() method. We update the hash object with each chunk using the update() method. Finally, we return the hex digest of the hash object using the hexdigest() method.

## Testing the function

Once we have defined the function to get the MD5 hash of a big file, we can test it by passing the filename to the function. For example:

```python
filename = "bigfile.iso"
md5 = get_file_md5(filename)
print("MD5 hash of", filename, "is", md5)
```

In the above code, we first define the filename of the big file we want to hash. Then, we call the get_file_md5() function with the filename as an argument and store the result in the variable md5. Finally, we print the filename and its corresponding MD5 hash.

## Full code

The complete code to get the MD5 hash of big files in Python is as follows:

```python
import hashlib

def get_file_md5(filename):
    hash_md5 = hashlib.md5()
    with open(filename, "rb") as f:
        while True:
            chunk = f.read(4096)
            if not chunk:
                break
            hash_md5.update(chunk)
    return hash_md5.hexdigest()

filename = "bigfile.iso"
md5 = get_file_md5(filename)
print("MD5 hash of", filename, "is", md5)
```

In this code, we first import the hashlib library. Then, we define the function to get the MD5 hash of a file in chunks. We test the function by passing the filename to it and print the result.
