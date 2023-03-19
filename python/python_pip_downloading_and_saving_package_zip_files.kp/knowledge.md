---
title: What steps should be followed to utilize python's pip for acquiring and retaining the compressed files associated with a package?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the command `pip download <package\_name> --dest <directory\_path>` to download and save the zipped files for a package.
---

**Contents**

[TOC]

## Introduction

`pip` is a package management system used to install and manage software libraries and dependencies written in Python. Sometimes, we may want to download and keep the zipped files for a particular package manually, so that we can use it later without having to download it again. In this tutorial, we will explore how to use `pip` to download and keep the zipped files for a package.


## Step 1: Install the Package

To download and keep the zipped files for a package, we first need to install the package using `pip`. We can do this by running the following command in a terminal or command prompt:

```
pip install <package-name>
```

Replace `<package-name>` with the name of the package you want to install.


## Step 2: Locate the Installed Package

After installing the package, we need to locate the directory where the package was installed. We can do this by using the following command:

```
pip show <package-name>
```

This command will display information about the installed package, including the location of the package directory. Note down the location of the package directory.


## Step 3: Compress the Package Directory

Next, we need to compress the package directory into a ZIP file. We can do this using any compression tool, such as `zip` or `tar`. For example, if the package directory is located at `/usr/local/lib/python3.9/site-packages/package-name`, we can compress it into a ZIP file named `package-name.zip` using the following command:

```
zip -r package-name.zip /usr/local/lib/python3.9/site-packages/package-name
```

The `-r` option tells the `zip` command to compress the directory recursively.


## Step 4: Keep the ZIP File

Finally, we can keep the ZIP file in a safe location for later use. We can also delete the original package directory if we don't need it anymore. To use the package in the future, simply unzip the ZIP file and place it in the appropriate directory (e.g., `/usr/local/lib/python3.9/site-packages/`).


## Conclusion

In this tutorial, we have learned how to use `pip` to download and keep the zipped files for a package. By following the above steps, we can easily save a copy of a package for future use, without having to download it again.
