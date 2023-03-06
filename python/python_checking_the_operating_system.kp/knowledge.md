---
title: What is the method to verify the operating system using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the sys module and its sys.platform attribute to check the operating system in Python.
---

**Contents**

[TOC]

## Importing the platform module
One way to check the operating system in Python is by using the **platform** module which provides an interface to access platform-specific information, including the operating system. To use this, we'll need to import the module using the following code:

```python
    import platform
```

## Using platform.system()
After importing the **platform** module, we can use the **system()** method to get the name of the operating system. The **system()** method returns the name of the operating system in lowercase letters. To get the name of the operating system, we can use the following code:

```python
    os_name = platform.system()
    print(os_name)
```

This code will print the name of the operating system such as **Windows**, **Linux**, **Darwin** (for macOS), **Java** (for Jython) among others.

## Using platform.platform()
Alternatively, we can use the **platform()** method to get more detailed information about the operating system. The **platform()** method returns a string that includes the operating system name, version, and architecture. To get more detailed information about the operating system, we can use the following code:

```python
    os_info = platform.platform()
    print(os_info)
```

This code will print a string that includes the operating system name, version, and architecture. 

## Using sys.platform
Another alternative strategy is to use the **sys** module to get information about the operating system. Specifically, the **sys.platform** property returns a string that identifies the platform on which Python is running. For instance, the returned string may be "linux", "linux2", "darwin", "win32", "freebsd7", or "openbsd4". We can use it as follows:

```python
    import sys

    os = sys.platform
    print(os)
```

This code will print the identifier string for the platform, such as "win32" for Windows or "darwin" for macOS.
