---
title: The installation of a Python package failed due to a clang error indicating that the argument '-mno-fused-madd' is unknown
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The `-mno-fused-madd` flag is no longer supported in newer versions of the clang compiler, causing an error during installation of certain Python packages.
---

**Contents**

[TOC]

Section 1: Background

When installing a Python package, users may encounter various errors related to the underlying system's configuration. One of these errors relates to the use of the '-mno-fused-madd' argument in the Clang compiler. This error can prevent successful installation of the Python package, leading to frustration and delays in development efforts.

Section 2: Explanation

The '-mno-fused-madd' argument is an optimization flag that was used in older versions of Clang. It was intended to improve performance by enabling a specific type of floating-point arithmetic operation called "fused multiply-add." However, this flag has since been deprecated, meaning it is no longer supported or recognized by modern versions of Clang.

When attempting to install a Python package, the installer may encounter the '-mno-fused-madd' argument and fail, as the compiler does not recognize the option. This results in a "compiler error" or "build failure," preventing the package from being installed correctly.

Section 3: Fix

To resolve this issue, users may need to modify the build process for the Python package. One potential solution is to disable the '-mno-fused-madd' argument by passing a different set of compiler flags during the installation process. This can be done by modifying the setup.py file for the package and adding the appropriate compiler flags to the "extra_compile_args" and "extra_link_args" variables. Alternatively, users can modify the compiler directly to remove the '-mno-fused-madd' option.

Section 4: Conclusion

In summary, the '-mno-fused-madd' error is a common issue that can arise when installing Python packages. This error occurs when an outdated compiler flag is encountered, preventing the installation process from completing correctly. To resolve this error, users can modify the build process for the Python package or modify the compiler directly to remove the problematic flag. By taking these steps, users can ensure that the Python package installs correctly and is ready to use in their development efforts.
