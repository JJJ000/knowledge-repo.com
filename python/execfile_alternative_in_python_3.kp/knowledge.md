---
title: What is a substitute for execfile in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The alternative to execfile in Python 3 is the exec() function.
---

**Contents**

[TOC]

1. Using `exec()` Function 

The `exec()` function can be used as an alternative to `execfile()` in Python 3. It takes a string containing Python code, compiles it, and then executes it. The syntax for `exec()` is as follows:

```
exec(object[, globals[, locals]])
```

Where `object` is a string of Python code, `globals` is a dictionary of global variables, and `locals` is a dictionary of local variables.

2. Using `execfile()` in Python 2 and `exec()` in Python 3

Another alternative is to use the `execfile()` function in Python 2 and `exec()` in Python 3. The syntax for `execfile()` is as follows:

```
execfile(filename[, globals[, locals]])
```

Where `filename` is the name of the file containing the Python code, `globals` is a dictionary of global variables, and `locals` is a dictionary of local variables.

3. Using `eval()` Function 

The `eval()` function can also be used as an alternative to `execfile()`. It takes a string containing Python code, compiles it, and then evaluates it. The syntax for `eval()` is as follows:

```
eval(expression[, globals[, locals]])
```

Where `expression` is a string of Python code, `globals` is a dictionary of global variables, and `locals` is a dictionary of local variables.

4. Using `exec()` and `eval()` Together

The `exec()` and `eval()` functions can also be used together to achieve the same effect as `execfile()`. The syntax for this is as follows:

```
exec(compile(open(filename).read(), filename, 'exec'), globals, locals)
```

Where `filename` is the name of the file containing the Python code, `globals` is a dictionary of global variables, and `locals` is a dictionary of local variables.
