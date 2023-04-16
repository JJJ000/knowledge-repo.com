---
title: No suitable c compiler was located in the $path directory when attempting to install python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You may need to install a compatible C compiler before installing Python.
---

**Contents**

[TOC]

**Step 1: Check if C Compiler is Installed**

The first step is to check if a C compiler is already installed on the system. This can be done by running the command `gcc --version` in the terminal. If a C compiler is installed, the command should return the version information.

**Step 2: Install C Compiler**

If the command does not return any information, then a C compiler needs to be installed. The easiest way to do this is to install the appropriate package from the package manager of the operating system. For example, on a Debian-based Linux distribution, the command `sudo apt-get install build-essential` can be used to install the build-essential package which includes the GNU C Compiler (GCC).

**Step 3: Configure Path**

Once the C compiler is installed, the PATH environment variable needs to be configured so that the compiler can be found. This can be done by adding the path of the compiler to the PATH variable. For example, if the GCC compiler is installed in the `/usr/bin` directory, the command `export PATH=$PATH:/usr/bin` can be used to add the path to the PATH variable.

**Step 4: Verify Installation**

The last step is to verify that the C compiler is working correctly. This can be done by running the command `gcc --version` again. If the command returns the version information of the compiler, then the installation was successful.
