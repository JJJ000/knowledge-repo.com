---
title: Is there a way to make pip reinstall the current version?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Yes, you can use the `-I` or `--force-reinstall` flag with pip to force a reinstall of the current version.
---

**Contents**

[TOC]

## Yes

1. Uninstall the current version of the package:
   ```
   pip uninstall <package_name>
   ```
2. Reinstall the current version of the package:
   ```
   pip install <package_name>
   ```

## No

1. If the package has been modified in some way, it is not possible to force pip to reinstall the current version. 
2. The only way to ensure the package is reinstalled correctly is to uninstall the current version and then install the desired version.
