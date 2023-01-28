---
title: Perform a git merge without automatically committing
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git merge can be done without auto commit by using the --no-commit option.
---

**Contents**

[TOC]

### Using `git merge --no-commit`

This option merges the specified branch into the current branch but does not make a commit. It allows you to review the changes and make any necessary adjustments before committing the merge.

### Syntax

```git
git merge --no-commit <branch-name>
```

### Example

To merge the `feature-branch` into the current branch without automatically committing the merge, you would run the following command:

```git
git merge --no-commit feature-branch
```

### Advantages

Using the `--no-commit` option allows you to review the changes before committing them, which can be useful if there are conflicts that need to be resolved or if you want to make changes to the merge commit message.
