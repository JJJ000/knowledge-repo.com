---
title: What is the process for deleting the initial commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git reset --hard <commit-id>` command, where <commit-id> is the id of the commit to be removed.
---

**Contents**

[TOC]

### Checkout the Commit

First, you need to checkout the commit you want to remove. You can do this by running the following command:

`git checkout <commit_hash>`

### Reset the Branch

Once you have checked out the commit, you can reset the branch to the previous commit. This will remove the commit you just checked out. To do this, run the following command:

`git reset --hard HEAD~1`

### Push the Changes

Finally, push the changes to the remote repository. This will overwrite the remote repository with the new changes. To do this, run the following command:

`git push -f`

### Clean Up

Once you have pushed the changes, you should clean up the local repository. This will remove any references to the commit you just removed. To do this, run the following command:

`git gc`
