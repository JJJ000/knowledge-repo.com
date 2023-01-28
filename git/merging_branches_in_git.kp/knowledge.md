---
title: What should be done with the branch after it has been merged?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: After a branch is merged into another branch in Git, it should be deleted to avoid confusion and reduce clutter.
---

**Contents**

[TOC]

### Delete the Branch
Once the merge is complete, the branch is no longer needed and can be deleted. This can be done with the following command:

```
git branch -d <branch_name>
```

### Push the Changes
After merging the branch, the changes need to be pushed to the remote repository. This can be done with the following command:

```
git push origin <branch_name>
```

### Check the Log
It's a good practice to check the git log to make sure the merge was successful. This can be done with the following command:

```
git log --graph --oneline --decorate
```

### Update Remote Branches
Finally, it's important to update the remote branches to make sure all changes are reflected. This can be done with the following command:

```
git remote update
```
