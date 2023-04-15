---
title: How do I change the name of a local Git branch?
authors:
- smart_coder
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use `git branch -m new-name` to rename the current local branch,
  or `git branch -m old-name new-name` to rename a different local branch.
---

**Contents**

[TOC]

### Rename the current local Git branch

To change the name of a Git branch, you can use the git branch command with the `-m` option followed by the new name you want to give to the branch. Here's the syntax:

```shell
git branch -m new-name
```

This will rename the current branch to `new-name`.

### Rename a different local Git branch

If you want to rename a different branch, you can use the git branch command followed by the old name and the new name, like this:

```shell
git branch -m old-name new-name
```

### Update the corresponding remote Git branch

If you want to update the name of the corresponding remote branch, you will need to use the `git push` command to push the updated branch to the remote repository. You can do this by using the `-u` option, like this:

```shell
git push -u origin new-name
```

This will set the new-name branch as the upstream branch for the local new-name branch, and any future git push or git pull commands will use this branch.
