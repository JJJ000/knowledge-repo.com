---
title: It is impossible to configure the default Python version to python3 on ubuntu
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the command `sudo update-alternatives --install /usr/bin/python Python /usr/bin/python3 1` to set the default Python version to python3.
---

**Contents**

[TOC]

Solution to Setting Default Python Version to Python3 in Ubuntu

Here are some of the solutions to set the default python version to python3 in Ubuntu:

1. Check Python Versions Installed

Before setting the default python version, check the versions already installed.

To do that, run the following command in the terminal:

```
$ ls /usr/bin/python*
```

The command output shows the python versions installed in the system:

```
/usr/bin/python   /usr/bin/python2  /usr/bin/python2.7
```

2. Install Additional Python Versions

If the python version required is not available in the system, install it.

To install python3, run the command:

```
$ sudo apt-get install python3
```

This command installs python3 in the system.

3. Configure alternatives

To configure the default python version, use the update-alternatives command.

Use the following command to configure python3 as the default python version:

```
$ sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 1
```

This command adds python3 as an alternative and assigns a priority of 1.

Use the following command to configure python2 as the default python version:

```
$ sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 2
```

This command adds python2 as an alternative and assigns a priority of 2.

4. Select the Default Python Version

To select the default python version, use the update-alternatives command.

Use the following command to select python3 as the default python version:

```
$ sudo update-alternatives --config python
```

This command shows a list of python versions available in the system.

Select python3 by typing the number shown before python3 and pressing Enter.

That's it. Now python3 is set as the default python version in Ubuntu.
