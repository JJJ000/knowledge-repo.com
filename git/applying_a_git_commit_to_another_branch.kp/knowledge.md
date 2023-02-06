---
title: Apply a commit from another branch to the working copy using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use `git cherry-pick` to apply a commit from another branch to the working copy.
---

**Contents**

[TOC]

## Checkout the Desired Branch

To apply a commit from one branch to the working copy, the first step is to checkout the desired branch. This can be done with the following command:

```
git checkout <branch_name>
```

## Cherry Pick the Commit

Once the desired branch has been checked out, the next step is to cherry pick the commit. This can be done with the following command:

```
git cherry-pick <commit_hash>
```

This will apply the commit to the current branch.

## Push Changes

Once the commit has been applied to the current branch, the changes need to be pushed to the remote repository. This can be done with the following command:

```
git push origin <branch_name>
```

## Verify Changes

Finally, the changes should be verified to ensure that the commit was applied correctly. This can be done by checking the commit history of the branch or by running tests to ensure that the changes have been applied correctly.
