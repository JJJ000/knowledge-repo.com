---
title: What git command can I use to see which files are being ignored by .gitignore?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The `git check-ignore` command can be used to show which specific files are ignored by .gitignore.
---

**Contents**

[TOC]

### git check-ignore

The `git check-ignore` command allows you to check which files are being ignored by `.gitignore` rules. It takes a pathname as an argument, and it returns the name of the file or directory and the rule that is ignoring it.

### Syntax

The syntax for `git check-ignore` is as follows:

```
git check-ignore [-v] [--no-index] [--stdin] [--] <pathname>…
```

### Examples

For example, to check which files are being ignored in the current directory, you can run the following command:

```
git check-ignore .
```

To check which files are being ignored in a specific directory, you can run the following command:

```
git check-ignore path/to/directory
```
