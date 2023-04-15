---
title: What is the best way to ensure that git uses lf instead of cr+lf on a windows machine?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git config core.autocrlf true` to force Git to use LF instead of CR+LF under Windows.
---

**Contents**

[TOC]

### Configuring Git
1. Open the Git Bash command line interface.
2. Type the following command: `git config --global core.autocrlf false`

### Setting File Attributes
1. Right-click on the file in Windows Explorer.
2. Select `Properties`.
3. Select the `Advanced` button.
4. Check the box for `Keep both character sets (LF and CRLF)`.

### Configuring Text Editors
1. Open the text editor of your choice.
2. Go to the settings and select `Line Endings`.
3. Select `LF` as the line ending type.

### Verifying Settings
1. Open the file in the text editor of your choice.
2. Check the line endings of the file.
3. If they are LF, the settings have been successfully applied.
