---
title: Retrieve a file from an earlier commit in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Check out the commit using `git checkout <commit-SHA>` and then copy the file from the checked out commit.
---

**Contents**

[TOC]

# Step 1: Checkout the Commit
To restore a file from an old commit, the first step is to checkout the commit. This can be done using the `git checkout` command.

# Step 2: Check the File
Once the commit has been checked out, the file can be checked to make sure it is the correct version. This can be done using the `git show` command.

# Step 3: Restore the File
To restore the file, the `git checkout` command can be used with the `-- <file>` option. This will restore the file to the version in the commit.

# Step 4: Commit the Changes
Finally, the changes can be committed using the `git commit` command. This will create a new commit containing the restored file.
