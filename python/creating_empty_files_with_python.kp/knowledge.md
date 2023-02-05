---
title: Make an empty file with python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: open(`filename.txt`, `w`).close()
---

**Contents**

[TOC]

# Section 1: Create a File
The following code will create an empty file using Python:

```
open('filename.txt', 'w').close()
```

# Section 2: File Path
By default, the file will be created in the same directory as the Python script. To specify a different directory, you can use an absolute or relative path:

```
open('/path/to/filename.txt', 'w').close()
open('../path/to/filename.txt', 'w').close()
```

# Section 3: Writing to the File
Once the file is created, you can write to it using the `write()` method:

```
with open('filename.txt', 'w') as f:
    f.write('Hello World!')
```

# Section 4: Appending to the File
If you want to append to the file instead of overwriting it, you can use the `append()` method:

```
with open('filename.txt', 'a') as f:
    f.write('Hello World!')
```
