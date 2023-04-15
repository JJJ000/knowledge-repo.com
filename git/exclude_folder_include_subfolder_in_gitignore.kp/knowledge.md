---
title: Include all files and folders in the '.gitignore' file except for a specific subfolder
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Yes, you can use `!` to negate a pattern and specify a subfolder to include.
---

**Contents**

[TOC]

### Excluding a Folder

To exclude a folder, add the folder name to the `.gitignore` file. For example, if you wanted to exclude the `docs` folder, you would add `docs/` to the `.gitignore` file.

### Including a Subfolder

To include a specific subfolder, you can add the path to the subfolder in the `.gitignore` file. For example, if you wanted to include the `docs/subfolder` subfolder, you would add `!docs/subfolder/` to the `.gitignore` file.

### Using Wildcards

You can also use wildcards in the `.gitignore` file to include or exclude specific files or folders. For example, if you wanted to exclude all files in the `docs` folder except for `.txt` files, you would add `docs/*.txt` to the `.gitignore` file.

### Summary

In summary, you can use the `.gitignore` file to exclude entire folders and include specific subfolders. You can also use wildcards to include or exclude specific files and folders.
