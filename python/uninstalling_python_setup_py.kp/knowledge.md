---
title: Uninstall Python using the setup.py script
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: No, the command to uninstall a package is `pip uninstall <package-name>`.
---

**Contents**

[TOC]

# Uninstalling the Package

The setup.py file is used to install a package in Python. To uninstall a package, the same setup.py file can be used.

## Steps
1. Navigate to the directory containing the setup.py file.
2. Run the command `python setup.py uninstall`
3. The package will be uninstalled.

## Notes
- The command will only uninstall the package if it was previously installed using the setup.py file.
- If the package was installed using other methods, the setup.py file will not be able to uninstall the package.
