---
title: Instructions for reverting changes using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To revert a commit, use the `git revert` command followed by the commit hash.
---

**Contents**

[TOC]

# Section 1: Overview

Git Revert is a command used to undo changes to a file or files in a Git repository. This command can be used to reverse changes to a single file, multiple files, or even an entire commit. It is important to note that the revert command does not delete the changes, but instead creates a new commit with the opposite changes.

# Section 2: Syntax

The syntax for the git revert command is as follows:

```
git revert <commit>
```

Where <commit> is the commit that you want to revert.

# Section 3: Examples

To revert a single file, use the following command:

```
git revert HEAD -- <file>
```

Where <file> is the file that you want to revert.

To revert multiple files, use the following command:

```
git revert HEAD -- <file1> <file2> <file3>
```

Where <file1>, <file2>, and <file3> are the files that you want to revert.

# Section 4: Tips

It is important to note that the git revert command does not delete the changes, but instead creates a new commit with the opposite changes. This means that the changes you are reverting will still be visible in the repository’s history.

It is also important to be careful when using the git revert command, as it can easily undo changes that you may not have intended to undo. It is a good practice to use the git diff command to review the changes that will be reverted before executing the git revert command.
