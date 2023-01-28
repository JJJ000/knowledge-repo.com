---
title: How to incorporate changes to a file into an earlier (not most recent) commit using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use `git cherry-pick <commit-hash>` to add a changed file to an older commit.
---

**Contents**

[TOC]

### Checkout the Desired Commit

To add a changed file to an older commit, you must first checkout that commit. This can be done by running `git checkout <commit-hash>`, where `<commit-hash>` is the hash of the commit you want to add the file to.

### Add the File

Once you have checked out the desired commit, you can add the file you want to the commit. This can be done by running `git add <file>`, where `<file>` is the path to the file you want to add.

### Commit the File

Once you have added the file, you can commit it to the repository. This can be done by running `git commit -m "<message>"`, where `<message>` is the commit message you want to use.

### Push the Commit

Finally, you can push the commit to the repository by running `git push origin <branch>`, where `<branch>` is the branch you are pushing the commit to.
