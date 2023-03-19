---
title: It is not possible to install lxml on mac os x 10.9
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can install Lxml on Mac OS X 10.9 in Python using pip or easy\_install commands in the terminal.
---

**Contents**

[TOC]

Section 1: The Problem

The problem is that when trying to install Lxml on a Mac OS X 10.9 system with Python, the process fails with different error messages, such as "Command 'clang' failed with exit status 1", "ld: library not found for -lz", or "fatal error: 'libxml/xmlversion.h' file not found".

Section 2: The Solution

The solution is to first install the necessary dependencies that Lxml requires, such as libxml2, libxslt, and zlib, using a package manager like Homebrew. Then, we can try installing Lxml using pip or by building it from source.

Section 3: Installing Dependencies

1. Install Homebrew if not already installed: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
2. Install libxml2: `brew install libxml2`
3. Install libxslt: `brew install libxslt`
4. Install zlib: `brew install zlib`

Section 4: Installing Lxml

1. Try installing Lxml using pip: `pip install lxml`
2. If pip fails, try installing Lxml by building it from source:
	1. Download the Lxml source code from https://pypi.org/project/lxml/#files and extract it.
	2. `cd` into the extracted directory.
	3. Run the following commands, replacing `<path_to_libraries>` with the actual paths to the libraries installed in section 3:		
		```
		C_INCLUDE_PATH=<path_to_libraries>/include LIBRARY_PATH=<path_to_libraries>/lib python setup.py build
		sudo C_INCLUDE_PATH=<path_to_libraries>/include LIBRARY_PATH=<path_to_libraries>/lib python setup.py install
		```
	4. Lxml should now be installed successfully.

Note: If the above solution does not work, it may be necessary to install a different version of Lxml, or to upgrade or downgrade Python and its dependencies. Further troubleshooting may be required.
