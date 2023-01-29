---
title: Re-wording 'null object in python'
python's null object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A None object is a null object in Python which represents nothing and holds no value.
---

**Contents**

[TOC]

#### Definition
A NoneType object in Python is a special object that represents the absence of a value. It is a null value and is equivalent to the value None.

#### Usage
The NoneType object is used as a placeholder when a value is not available or when a value is not applicable. It is also used to indicate the end of a list or a sequence.

#### Example
For example, if a function does not return a value, it will return a NoneType object.

```python
def my_function():
    # some code
    
result = my_function()

print(result) # prints None
```

#### Comparison to Other Languages
In other languages, such as Java, NoneType is represented as null.
