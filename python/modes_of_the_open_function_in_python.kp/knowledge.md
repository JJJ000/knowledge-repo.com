---
title: What are the distinctions between the modes a, a+, w, w+, and r+ when using the built-in open function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The modes a, a+, w, w+, and r+ indicate whether the file should be opened in read (`r`), write (`w`), append (`a`), or read and write (`+`) mode.
---

**Contents**

[TOC]

# Mode a

Mode a is used to open a file for appending. It is used to add content to the existing file, and if the file does not exist, it is created.

# Mode a+

Mode a+ is used to open a file for both reading and appending. It is used to add content to the existing file, and if the file does not exist, it is created.

# Mode w

Mode w is used to open a file for writing. It is used to overwrite the existing file, and if the file does not exist, it is created.

# Mode w+

Mode w+ is used to open a file for both reading and writing. It is used to overwrite the existing file, and if the file does not exist, it is created.

# Mode r+

Mode r+ is used to open a file for both reading and writing. It is used to read and write to the existing file, and if the file does not exist, it will not be created.
