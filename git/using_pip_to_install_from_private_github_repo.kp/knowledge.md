---
title: Can pip be used to install a package from a private github repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, it is possible to use pip to install a package from a private GitHub repository by providing the repository URL.
---

**Contents**

[TOC]

### Yes

Yes, it is possible to use pip to install a package from a private GitHub repository.

### Steps

1. Create a personal access token in GitHub.
2. Use the token to generate a secure URL for the repository.
3. Install the package using the secure URL with the `pip install` command.

### Example

For example, if the repository URL is `https://github.com/username/my_package`, the secure URL for the repository can be generated using the command `pip install git+https://<token>@github.com/username/my_package.git`.

### Note

It is important to note that the personal access token should only be used for the purpose of installing the package and should not be shared with anyone else.
