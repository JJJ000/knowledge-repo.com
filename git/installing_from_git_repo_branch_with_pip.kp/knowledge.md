---
title: Install a package from a git repository branch using pip
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To install a package from a Git repository branch, use the pip install command followed by the Git URL and the branch name.
---

**Contents**

[TOC]

### Using a Requirements File

1. Create a `requirements.txt` file in the root directory of your project.
2. Add the following line to the requirements file, replacing `<repo-url>` and `<branch-name>` with the appropriate values for your project:
```
-e git+<repo-url>@<branch-name>#egg=<package-name>
```
3. Install the package using pip:
```
pip install -r requirements.txt
```

### Using pip Directly

1. Install the package using pip, replacing `<repo-url>` and `<branch-name>` with the appropriate values for your project:
```
pip install git+<repo-url>@<branch-name>
```
2. To upgrade the package to the latest version of the branch, run:
```
pip install --upgrade git+<repo-url>@<branch-name>
```
