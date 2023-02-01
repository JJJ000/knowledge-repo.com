---
title: What does the Python keyword "with" do?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The `with` keyword in Python is used to wrap the execution of a block of code within a context manager.
---

**Contents**

[TOC]

#### Definition
The keyword "with" is used to simplify exception handling when using the "try/finally" statement. It is used to wrap the execution of a block with methods defined by a context manager.

#### Syntax
The syntax for the "with" keyword is as follows:

```
with expression [as variable]:
    with-block
```

#### Example
An example of the "with" keyword in use is as follows:

```
with open("file.txt") as f:
    data = f.read()
```

In this example, the file "file.txt" is opened and the contents are read into the variable "data" using the "with" keyword. The file is automatically closed at the end of the block.
