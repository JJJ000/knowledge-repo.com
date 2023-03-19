---
title: What is the method for removing a package installed using the pip install --user command?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the command `pip uninstall <package\_name>` to uninstall a package installed with `pip install --user` in Python.
---

**Contents**

[TOC]

# Checking installed packages

Before uninstalling a package installed with `pip install --user`, it's important to know the package name and version currently installed. To check the list of installed packages, run the following command in the terminal:

```
pip list --user
```

This will display a list of all packages installed using the `--user` flag.

# Uninstalling a package

To uninstall a package installed with `pip install --user`, run the following command in the terminal:

```
pip uninstall <package-name>
```

Replace `<package-name>` with the name of the package you wish to uninstall. You'll be prompted to confirm the uninstallation. 

For example, to uninstall the package `numpy`, run the following command:

```
pip uninstall numpy
```

# Removing package files

After uninstalling a package, its files may still be present on your system. You can remove these leftover files using the `pip uninstall` command with the `--user` and `--yes` flags, like this:

```
pip uninstall <package-name> --user --yes
```

This will remove any remaining files associated with the package you uninstalled. 

# Conclusion

In this article, you learned how to uninstall a package installed with `pip install --user` in Python by checking for installed packages, uninstalling the package, and removing any leftover files.
