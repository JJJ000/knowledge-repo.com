---
title: What is the method for repeating the previous command in the Python interpreter shell?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: In the Python interpreter shell, use the up arrow key to repeat the previous command.
---

**Contents**

[TOC]

# Introduction

Python interpreter shell provides an interactive environment to execute python code. It allows the user to execute python code line by line in real-time. Sometimes we may need to repeat the last command that we entered in the python interpreter shell. In this tutorial, we will learn how to repeat the last command in the python interpreter shell.

# Using Underscore (_)

In the Python interpreter shell, we can use the underscore character ( _ ) to repeat the last command. When we use the underscore character, it represents the output of the last executed command.

```
>>> 2 + 3
5
>>> _
5
```

In the above example, we can see that we have used the underscore character to repeat the last command, which was `2 + 3`.

# Using the Up Arrow

In the Python interpreter shell, we can also use the up arrow key to repeat the last command. When we use the up arrow key, it shows the last entered command, and we can modify it if needed.

```
>>> 2 + 3
5
>>> <up arrow>
2 + 3
```

In the above example, we have used the up arrow key to repeat the last command, which was `2 + 3`.

# Using the History Command

In addition to the above methods, the Python interpreter shell also has a history command that allows us to see the history of executed commands. We can use the history command to find the last executed command and repeat it.

```
>>> 2 + 3
5
>>> history
1. 2 + 3
2. history
>>> exec( history[-2] )
5
```

In the above example, we have used the history command to see the executed commands' history. After that, we have used the `exec` command to execute the last command, which was `2 + 3`.

# Conclusion

In this tutorial, we have learned how to repeat the last command in the python interpreter shell using the underscore character, up arrow key, and history command. These methods can help us save time and make our workflow more efficient.
