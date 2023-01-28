---
title: Revert a git merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To rollback a Git merge, use the command `git merge --abort`.
---

**Contents**

[TOC]

### Checkout Merge Commit

To rollback a git merge, the first step is to check out the merge commit. This can be done by running the following command:

```git
git checkout -b <branch-name> <merge-commit-SHA>
```

Where `<branch-name>` is a name for the branch you will create and `<merge-commit-SHA>` is the SHA of the merge commit you wish to rollback.

### Reset the Repository

Once you have checked out the merge commit, the next step is to reset the repository to the desired state. This can be done by running the following command:

```git
git reset --hard <desired-commit-SHA>
```

Where `<desired-commit-SHA>` is the SHA of the commit you wish to reset the repository to.

### Push Changes

The final step is to push the changes to the remote repository. This can be done by running the following command:

```git
git push -f <remote> <branch-name>
```

Where `<remote>` is the name of the remote repository and `<branch-name>` is the name of the branch created in the first step.
