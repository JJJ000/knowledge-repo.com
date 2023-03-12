---
title: Access files using 'rt' and 'wt' modes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: `rt` mode is used to open a file in read mode and `wt` mode is used to open a file in write mode in Python.
---

**Contents**

[TOC]

Opening Files in 'rt' Mode

The 'rt' mode is used to open a file in text mode, meaning that the data in the file is treated as text. To open a file in 'rt' mode in Python, you can use the built-in function open() and specify the mode parameter as 'rt'. Here's an example:

```
with open('myfile.txt', 'rt') as f:
    # do something with the file
```

In the above code, 'myfile.txt' is the name of the file you want to open, and 'rt' is the mode you want to open it in. The 'with' statement ensures that the file is closed properly after you're done with it.

Opening Files in 'wt' Mode

The 'wt' mode is used to open a file for writing text content. In order to open a file in 'wt' mode in Python, you can use the open() function and specify the mode parameter as 'wt'. Here's an example:

```
with open('myfile.txt', 'wt') as f:
    f.write('Hello, world!')
```

In the above code, 'myfile.txt' is the name of the file you want to write to, and 'wt' is the mode you want to open it in. We use the write() function to write the string 'Hello, world!' to the file.

Closing Files

It's important to close files after you're done with them, so that the system resources used by the file can be freed up. In Python, you can use the close() method to close a file. However, it's often more convenient to use the 'with' statement, as shown in the examples above. This ensures that the file is closed automatically when you're done with it, even if an error occurs while processing the file.
