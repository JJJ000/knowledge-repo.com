---
title: Revert the last commit on a remote git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To remove the last commit from a remote Git repository, use the `git push <remote> --force <branch>` command.
---

**Contents**

[TOC]

### Solution

### Checkout the Previous Commit
To remove the last commit from a remote Git repository, the first step is to checkout the previous commit. This can be done by running the following command:

```git
git checkout HEAD~1
```

### Revert the Last Commit
Once the previous commit is checked out, the next step is to revert the last commit. This can be done by running the following command:

```git
git revert HEAD
```

### Push the Reverted Commit
Finally, the reverted commit needs to be pushed to the remote repository. This can be done by running the following command:

```git
git push origin master
```

### Verify the Changes
To verify that the last commit has been successfully removed from the remote repository, you can run the following command:

```git
git log
```

This will show the history of commits in the repository and should no longer include the last commit.
