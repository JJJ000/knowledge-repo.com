---
title: Could I have a list of files that have been marked as '--assume-unchanged'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can use the command `git ls-files -v | grep `^h`` to get a list of files marked --assume-unchanged in Git.
---

**Contents**

[TOC]

### Listing Files

To list all files marked as `--assume-unchanged` in Git, use the following command:

```git
git ls-files -v | grep '^[hsmrck]'
```

### Explaining the Output

The output of the command will list all files that have been marked as `--assume-unchanged` in the repository. The output will look something like this:

```git
h <filename>
```

The `h` indicates that the file is marked as `--assume-unchanged`.

### Unmarking Files

To unmark a file as `--assume-unchanged`, use the following command:

```git
git update-index --no-assume-unchanged <filename>
```

This will unmark the file and allow it to be tracked again.

### Resetting All Files

To reset all files marked as `--assume-unchanged` in the repository, use the following command:

```git
git update-index --assume-unchanged $(git ls-files -v | grep '^[hsmrck]' | awk '{print $2}')
```

This will reset all files marked as `--assume-unchanged` in the repository.
