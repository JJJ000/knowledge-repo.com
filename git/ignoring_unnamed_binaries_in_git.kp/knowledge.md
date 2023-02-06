---
title: Exclude binary files without an extension from the git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, you cannot ignore binary files that have no extension.
---

**Contents**

[TOC]

# Using a Wildcard

It is possible to use a wildcard to ignore binary files that have no extension. To do this, add the following line to the `.gitignore` file:

`*`

# Using a Script

Alternatively, you can write a script to ignore binary files that have no extension. The script should look for files with no extension and add them to the `.gitignore` file.

# Using a Command

It is also possible to use the command line to ignore binary files that have no extension. The following command can be used to add all files with no extension to the `.gitignore` file:

`find . -type f -name '*.*' -not -name '*.*.*' -exec echo '{}' >> .gitignore \;`

# Using a GUI Tool

Finally, there are several GUI tools available that can be used to ignore binary files with no extension. These tools provide an easy way to add files to the `.gitignore` file without having to manually edit the file.
