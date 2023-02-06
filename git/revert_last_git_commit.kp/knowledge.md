---
title: Revert the last git commit to the unstaged area
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To undo the last commit and move the changes to the unstaged area, use `git reset HEAD~1`.
---

**Contents**

[TOC]

# Section 1: Removing the Last Commit

1. To remove the last commit, type the following command into the terminal:
```
git reset --soft HEAD~1
```

# Section 2: Unstaging the Changes

2. To move the changes from the last commit to the unstaged area, type the following command into the terminal:
```
git reset
```

# Section 3: Verifying the Changes

3. To verify that the changes from the last commit have been moved to the unstaged area, type the following command into the terminal:
```
git status
```

# Section 4: Committing the Changes

4. To commit the changes to the unstaged area, type the following command into the terminal:
```
git commit -m "Commit message"
```
