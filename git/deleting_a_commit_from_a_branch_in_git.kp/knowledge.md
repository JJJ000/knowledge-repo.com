---
title: What is the process for removing a commit from a branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To delete a commit from a branch in Git, use the `git revert` command.
---

**Contents**

[TOC]

### Checkout the Branch

To delete a commit from a branch in Git, the first step is to checkout the branch that contains the commit. This can be done by running the following command:

```shell
git checkout <branch-name>
```

### Revert the Commit

Once the branch is checked out, the next step is to revert the commit that needs to be removed. This can be done by running the following command:

```shell
git revert <commit-hash>
```

### Push the Reverted Commit

After the commit has been reverted, the changes need to be pushed to the remote repository. This can be done by running the following command:

```shell
git push origin <branch-name>
```

### Cleanup the Branch

Finally, the branch needs to be cleaned up to ensure that the commit is completely removed. This can be done by running the following command:

```shell
git branch -D <branch-name>
```
