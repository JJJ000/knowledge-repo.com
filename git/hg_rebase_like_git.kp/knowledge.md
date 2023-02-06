---
title: How can I perform a rebase similar to the one done in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In Mercurial, a rebase can be done with the `rebase` command.
---

**Contents**

[TOC]

1. **Preparation:** 
   Before you start a rebase, it is important to make sure that all changes have been committed and pushed to the remote repository. If you are rebasing onto a branch, make sure that the branch is up to date with the remote repository.

2. **Rebase:** 
   To start a rebase, use the `hg rebase` command. This will start the rebase process, which will replay the commits from the current branch onto the destination branch.

3. **Resolve Conflicts:** 
   During the rebase process, conflicts may arise if the same lines of code have been modified in both branches. In this case, you will need to manually resolve the conflicts before continuing with the rebase.

4. **Finish the Rebase:** 
   Once all conflicts have been resolved, you can finish the rebase by running the `hg rebase --continue` command. This will complete the rebase and update the repository with the new changes.
