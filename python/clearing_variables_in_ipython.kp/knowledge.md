---
title: What is the procedure for clearing variables in ipython?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Type `%reset` in the ipython console and press enter.
---

**Contents**

[TOC]

## Introduction

IPython is an interactive shell that offers enhanced features like shell-like commands, object introspection, and tab-completion. It allows users to experiment with code, test ideas, and debug programs. In this guide, we will show you how to clear variables in IPython.

## Viewing Variables

Before we clear the variables, let's first view the existing variables in IPython. To do this, we use the `%who` command:

```
%who
```

This will display all the variables that are currently defined in our session.

## Clearing Variables

To clear a variable, we can use the `del` command followed by the variable name. For example:

```
del my_variable
```

This will delete the variable called `my_variable`.

If we want to clear all the variables, we can use the `%reset` command. This will remove all variables, functions, and imports from the current IPython session. 

```
%reset
```

By default, this command will prompt us to confirm that we want to clear all variables. To skip the prompt and execute the reset command immediately, we can pass the `-f` (force) flag:

```
%reset -f
```

## Conclusion

In this guide, we have shown you how to clear variables in IPython. You can use the `del` command to delete individual variables or the `%reset` command to clear all variables at once. Remember to use these commands with caution, as they will permanently remove data from your session.
