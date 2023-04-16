---
title: What is the process for transforming a string representation of a list into an actual list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the built-in function `ast.literal\_eval` to convert a string representation of a list to an actual list.
---

**Contents**

[TOC]

# Section 1: Overview

In Python, it is possible to convert a string representation of a list (i.e. a string containing comma-separated values) into an actual list. This can be done using the built-in `ast.literal_eval()` function.

# Section 2: Syntax

The syntax for using `ast.literal_eval()` is as follows:

```
list_variable = ast.literal_eval(string_representation_of_list)
```

# Section 3: Example

For example, if we have the following string representation of a list:

```
string_list = "[1, 2, 3, 4, 5]"
```

We can convert it to a list using the following code:

```
import ast
list_variable = ast.literal_eval(string_list)
```

# Section 4: Output

The output of the above code would be:

```
[1, 2, 3, 4, 5]
```
