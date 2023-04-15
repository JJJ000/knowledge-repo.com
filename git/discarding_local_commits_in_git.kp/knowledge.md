---
title: What is the process for removing local commits in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To discard local commits in Git, use `git reset --hard HEAD~<number\_of\_commits>`.
---

**Contents**

[TOC]

### Step 1: Discard All Uncommitted Changes

If you want to discard all uncommitted changes in your working directory, you can use the `git reset --hard HEAD` command. This will reset your working directory to the most recent commit, discarding any changes that have not been committed.

### Step 2: Discard Specific Commits

If you want to discard specific commits, you can use the `git reset` command. This command takes a commit hash as an argument and will reset your working directory to the state of the commit prior to the one specified.

### Step 3: Push the New Commit

Once you have discarded the commits you want to discard, you will need to push the new commit to the remote repository. This can be done using the `git push` command.

### Step 4: Clean Up Your Local Repository

Finally, you should clean up your local repository by using the `git clean` command. This will remove any untracked files and directories from your working directory.
