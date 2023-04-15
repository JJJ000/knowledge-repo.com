---
title: What is the process for committing only certain files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use `git commit -m <message> <file1> <file2> ...` to commit only some files.
---

**Contents**

[TOC]

### Step 1: Staging

To commit only some files, first you need to stage the files you want to commit. This can be done by running the command `git add <file>` for each file you want to commit. 

### Step 2: Commit

Once you have staged the files you want to commit, you can commit them by running `git commit -m "<message>"`. The `-m` flag is used to add a commit message.

### Step 3: Push

Finally, to push the changes to the remote repository, run `git push`. This will push all committed changes to the remote repository.
