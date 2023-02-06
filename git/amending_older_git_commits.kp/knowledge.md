---
title: What is the process for modifying an existing git commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git commit --amend` to amend an older Git commit.
---

**Contents**

[TOC]

# Section 1: Preparation
1. Before amending an older commit, you should make sure that the changes you are making are necessary and that you have a good understanding of the code.
2. Make sure to commit any changes that you have made to the repository before amending the commit.

# Section 2: Amend the Commit
1. To amend an older commit, use the command `git commit --amend`.
2. This will open an editor window with the commit message of the older commit.
3. Edit the commit message to include the changes and save the file.

# Section 3: Push the Changes
1. After amending the commit, use the command `git push --force` to push the changes to the remote repository.
2. This will overwrite the older commit with the new amended commit.

# Section 4: Cleanup
1. After the commit has been amended, it is important to clean up any local changes that have been made.
2. This can be done by using the command `git reset --hard` to reset the local repository to the state of the remote repository.
