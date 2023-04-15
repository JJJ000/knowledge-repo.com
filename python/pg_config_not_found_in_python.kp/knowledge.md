---
title: The pg_config program could not be located
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The pg\_config executable must be installed separately and added to the PATH environment variable for Python to find it.
---

**Contents**

[TOC]

# Solution

## Overview

The pg_config executable is a utility program that is used to determine how the PostgreSQL server was compiled and installed. It is typically located in the bin directory of the PostgreSQL installation directory. When using the Python PostgreSQL interface, pg_config is used to determine the correct compiler flags and libraries needed to build the Python module.

## Problem

The problem arises when the pg_config executable is not found in the Python installation directory. This can happen if the PostgreSQL server was installed in a non-standard location or if the pg_config executable is not in the PATH environment variable.

## Solution

The solution is to manually specify the path to the pg_config executable in the Python installation directory. This can be done either by setting the environment variable PG_CONFIG or by passing the path as a command line argument to the Python setup.py script.

## Conclusion

In order to use the PostgreSQL interface with Python, it is necessary to make sure that the pg_config executable is in the PATH environment variable or manually specify the path to the executable. This ensures that the Python module can be built correctly and that the PostgreSQL server can be accessed from Python.
