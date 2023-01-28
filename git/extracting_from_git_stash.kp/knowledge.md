---
title: What is the process for retrieving a single file (or changes to a file) from a git stash?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git stash show <stash-name> -- <file-name>` to extract a single file (or changes to a file) from a git stash.
---

**Contents**

[TOC]

### 1. Checkout the Stash

To extract a single file (or changes to a file) from a git stash, first checkout the stash using the command `git stash apply`:

```git
git stash apply
```

This will apply the changes from the stash to the current working directory.

### 2. Extract the File

Once the stash is applied, use the command `git show` to extract the file (or changes to the file) from the stash:

```git
git show <stash-name>:<file-name>
```

The `<stash-name>` is the name of the stash and the `<file-name>` is the name of the file that you want to extract.

### 3. Save the File

Once the file is extracted, save it to the desired location.

### 4. Cleanup

Finally, clean up the stash by using the command `git stash drop`:

```git
git stash drop <stash-name>
```

This will remove the stash from the list of stashes.
