---
title: Install pip forcefully without considering dependencies
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To force install a package ignoring dependencies in Python using pip, use the command `pip install --no-deps package-name`.
---

**Contents**

[TOC]

# Introduction

Sometimes, during installation of a package using pip, we might want to force the installation and ignore any dependencies that might hold back the installation. This might be due to compatibility issues or simply because we don't need the installed package to work with any other packages.

In this article, we will discuss how to force install a package using pip while ignoring dependencies.

# Using the `--no-deps` option

The `--no-deps` option in pip skips the installation of any dependencies required by the package being installed. This can be used to force install a package and ignore its dependencies.

To install a package using pip while ignoring dependencies, we simply add the `--no-deps` option to the pip install command:

```
pip install package_name --no-deps
```

This will install the package `package_name` without installing any of its dependencies.

# Using the `--ignore-installed` option

The `--ignore-installed` option in pip ignores any previously installed versions of the package being installed. This can be used to force install a package and ignore any conflicts that might occur due to previously installed versions of the package.

To install a package using pip while ignoring previously installed versions, we simply add the `--ignore-installed` option to the pip install command:

```
pip install package_name --ignore-installed
```

This will install the latest version of `package_name` while ignoring any previously installed versions.

# Using the `--force-reinstall` option

The `--force-reinstall` option in pip forces a reinstallation of the package being installed even if it is already installed. This can be used to force install a package and overwrite any conflicts that might occur due to previously installed versions of the package.

To force reinstall a package using pip, we simply add the `--force-reinstall` option to the pip install command:

```
pip install package_name --force-reinstall
```

This will reinstall the latest version of `package_name` even if it was already installed.

# Conclusion

In this article, we looked at three methods that can be used to force install a package using pip while ignoring dependencies. These are the `--no-deps`, `--ignore-installed`, and `--force-reinstall` options. These options can be used to force install a package and overwrite any conflicts that might occur due to previously installed versions of the package.
