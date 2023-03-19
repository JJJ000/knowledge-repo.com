---
title: The installation of scipy on windows has encountered an issue in which lapack/blas resources cannot be found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The issue is resolved by installing the appropriate Lapack/Blas libraries on the system or using a pre-built Scipy package that includes them.
---

**Contents**

[TOC]

Section 1: Introduction

Scipy is a popular scientific computing library for Python that provides various functions for solving scientific calculations. It requires Lapack and Blas resources to work correctly. These libraries are responsible for providing fast and efficient linear algebra operations. When you install SciPy on your Windows computer and encounter the "No Lapack/Blas resources found" error, it means that you need to install these libraries manually.

In this article, we'll cover the solution to this problem in a step-by-step manner.

Section 2: Install Lapack/Blas on Windows

To install Lapack/Blas on Windows, follow these steps:

Step 1: Download the pre-built binaries of Lapack and Blas libraries from the following links:

- Lapack: http://icl.cs.utk.edu/lapack-for-windows/lapack/
- Blas: http://icl.cs.utk.edu/lapack-for-windows/libraries/Win32/

Step 2: Extract the downloaded files to a directory on your computer. For example, you can extract them to the C:\lapack and C:\blas directories.

Step 3: Add the directory containing the Lapack and Blas libraries to your PATH environment variable. To do this, follow these steps:

- Right-click on the Windows icon in the bottom-left corner of the screen and select "System".
- Click on "Advanced system settings".
- In the System Properties window, click on the "Environment Variables" button.
- In the "System Variables" section, scroll down and find the "Path" variable. Click on "Edit".
- Add the path to the directory containing the Lapack and Blas libraries to the end of the list. For example, add ";C:\lapack;C:\blas".

Step 4: Restart your computer for the changes to take effect.

Section 3: Verify Lapack/Blas Installation

To verify that Lapack/Blas is correctly installed and configured on your Windows computer, follow these steps:

Step 1: Open a command prompt by pressing the Windows key + R and typing "cmd" in the Run dialog box.

Step 2: Type "python" and press Enter.

Step 3: Type the following commands:

```python
import numpy as np
np.show_config()
```

Step 4: Look for the output that shows whether Lapack and Blas are being used for linear algebra operations. The output should contain something like the following:

```
lapack_info:
  libraries = ['lapack']
  library_dirs = ['C:/lapack']
  define_macros = [('HAVE_LAPACK_CONFIG_H', None)]
  language = f77
blas_info:
  libraries = ['blas', 'blas']
  library_dirs = ['C:/blas']
  define_macros = [('NO_ATLAS_INFO', 1), ('HAVE_CBLAS', None)]
  language = c
```

If you see this output, it indicates that Lapack and Blas are being used by NumPy, which is required for Scipy to work.

Section 4: Conclusion

Installing Lapack/Blas on Windows can be a bit tricky, but it's worth the effort as these libraries can significantly improve the performance of linear algebra operations in Scipy. By following the steps outlined in this article, you'll be able to install and configure Lapack/Blas on your Windows computer and get Scipy up and running in no time.
