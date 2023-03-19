---
title: Obtain the final output in the Python shell that allows user interaction
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can use the underscore character (\_) to access the result of the last evaluated expression in the interactive Python shell.
---

**Contents**

[TOC]

Using the Underscore Symbol
---

In the interactive Python shell, the underscore symbol `_` can be used to refer to the last result that was computed. The underscore is automatically assigned the value of the last expression that was evaluated.

For example, if we run the following commands:

```
>>> 2 + 2
4
>>> _ * 3
12
```

Then the result of the second command will be `12`, since `_` refers to the value of the last expression that was computed (`4` in this case). 


Using the `print` Function
---

Another way to display the value of the last expression that was evaluated is to use the `print` function. By wrapping an expression in the `print` function, we can see the result immediately.

For example, if we run the following commands:

```
>>> 3 * 5
15
>>> print(15)
15
```

Then `15` will be printed to the screen.


Using the History Feature
---

In some Python shells, there is a built-in history feature that records all of the commands that have been entered in the session. By using this feature, we can easily retrieve the last result that was computed.

For example, if we run the following commands:

```
>>> 10 - 3
7
>>> # use arrow up key to retrieve last command
>>> print(_)
7
```

Then the result of the `print` command will be `7`, since we used the arrow up key to retrieve the last command that was entered and then referred to its result using `_`.


Using the `input()` Function (for Python 3.x)
---

In Python 3.x, we can use the `input()` function to get the last result in the interactive shell. When we call `input()` with no argument, it will display the prompt `In [#]:`, where `#` is the next number in the sequence of commands entered in the session. We can then input the number of the command that we want to retrieve the result from.

For example, if we run the following commands:

```
>>> 2 * 8
16
>>> input()
In [2]:
2
Out[2]: 16
```

Then the result of the `input()` call will be `16`, since we input the number `2` to retrieve the result of the second command that was entered in the session.
