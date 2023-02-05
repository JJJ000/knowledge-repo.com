---
title: Will the file still be closed if I use a 'return' statement within a 'with' block in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, the file will still close when the `with` block is exited.
---

**Contents**

[TOC]

## Yes
When the control flow exits a `with` block, the `__exit__` method of the context manager object is called. This method is responsible for closing the file, so it will be closed even if you return inside the `with` block.

## Example

```python
with open('myfile.txt') as f:
    # do something
    return

# f is closed here
```

## Benefits
Returning inside a `with` block is a useful pattern when you want to exit early from a function. It allows you to avoid writing `f.close()` at the end of the function, making the code more concise and readable.

## Caveats
It's important to note that if an exception is raised inside the `with` block, the `__exit__` method will not be called, and the file will not be closed. In this case, it's necessary to use a `try-except` block to ensure the file is closed properly.
