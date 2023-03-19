---
title: The warning "runtimewarning numpy.dtype size changed, may indicate binary incompatibility" suggests that there could be a mismatch of binary versions in use
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: This warning suggests that there may be an issue with compatibility between different versions of numpy.
---

**Contents**

[TOC]

# What is the Issue?
The "RuntimeWarning: numpy.dtype size changed" warning typically occurs when the version of numpy being used by the user and the version that was used to compile a package (such as scikit-learn or pandas) are incompatible. Specifically, when numpy is updated to a new version, the package needs to be recompiled to use the new version.

# Why Does it Occur? 
This issue occurs because Python packages, such as scikit-learn, pandas, and matplotlib, are often compiled with a specific version of numpy. If a user upgrades to a newer version of numpy, the package may still be using the older version, which can cause compatibility issues and trigger this warning.

# How to Fix the Issue?
There are a few ways to address this issue:

1. Update the package: Try updating the package that is generating the warning to a version that is compatible with the newer version of numpy. This will generally involve uninstalling and then reinstalling the package using pip or conda.

2. Update numpy: If updating the package doesn't work, try updating numpy to a version that is compatible with the package. Again, this may require uninstalling and then reinstalling numpy.

3. Downgrade numpy: If you are unable to update the package or numpy, it may be necessary to downgrade numpy to the version specified in the package requirements.

4. Ignore the warning: If you cannot update the package or numpy, and downgrading numpy is not an option, you can choose to ignore the warning. However, this may cause unforeseen issues down the line, so it should be done with caution. To ignore the warning, you can add the following code at the beginning of your script:

import warnings
warnings.filterwarnings('ignore', 'numpy.dtype size changed')

# Conclusion:
Upgrading, Updating, or Downgrading numpy or the package to a compatible version or ignoring the warning is the best way to fix the numpy.dtype size changed warning.
