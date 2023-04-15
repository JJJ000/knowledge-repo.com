---
title: Ignore all files with the specified extension in the directory using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `echo `*.extension` > .gitignore` from the directory to ignore all files of the specified extension.
---

**Contents**

[TOC]

### Using Wildcards

You can use wildcards to ignore all files of a certain extension in a directory. For example, if you wanted to ignore all `.txt` files, you would add the following line to your `.gitignore` file:

```
*.txt
```

### Ignoring Specific Files

If you only want to ignore specific files of a certain extension, you can list the files individually in the `.gitignore` file. For example, if you wanted to ignore `file1.txt` and `file2.txt`, you would add the following lines to your `.gitignore` file:

```
file1.txt
file2.txt
```

### Ignoring a Directory

You can also ignore an entire directory and all of its contents. To do this, you would add the directory name to your `.gitignore` file. For example, if you wanted to ignore the `textfiles` directory, you would add the following line to your `.gitignore` file:

```
textfiles/
```

### Ignoring Multiple File Types

If you want to ignore multiple file types in a directory, you can use wildcards to specify multiple file extensions. For example, if you wanted to ignore all `.txt` and `.md` files, you would add the following line to your `.gitignore` file:

```
*.txt *.md
```
