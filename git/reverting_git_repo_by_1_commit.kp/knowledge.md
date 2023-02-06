---
title: Reverting the local and remote git repositories by one commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To roll back a local and remote git repository by 1 commit, use the command `git reset HEAD~1 --hard` followed by `git push -f origin <branch\_name>`.
---

**Contents**

[TOC]

**Rolling back Local Git Repository**

1. Checkout the Previous Commit: 
   To rollback the local repository to the previous commit, use the `git checkout` command followed by the commit hash or reference.

2. Reset the Head: 
   To reset the head to the previous commit, use the `git reset` command followed by the commit hash or reference.

**Rolling back Remote Git Repository**

1. Checkout the Previous Commit: 
   To rollback the remote repository to the previous commit, use the `git fetch` command followed by the remote repository URL and the commit hash or reference.

2. Reset the Head: 
   To reset the head to the previous commit, use the `git reset` command followed by the remote repository URL and the commit hash or reference.
