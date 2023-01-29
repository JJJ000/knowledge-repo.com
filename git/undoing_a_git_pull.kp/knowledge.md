---
title: What is the process for reverting a git pull?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git reset --hard HEAD@{1}` to undo the last pull.
---

**Contents**

[TOC]

### Step 1: Get the SHA of the Commit Before the Pull

To undo a git pull, the first step is to get the SHA of the commit before the pull. This can be done by running the following command:

`git log --oneline`

This command will output a list of all the commits in the repository, with each commit having its own SHA. Look for the commit that was made before the pull, and copy its SHA.

### Step 2: Reset the Repository

Once the SHA of the commit before the pull has been copied, the next step is to reset the repository to that commit. This can be done by running the following command:

`git reset --hard <SHA of Commit>`

This will reset the repository to the commit before the pull.

### Step 3: Push the Reset

The next step is to push the reset to the remote repository. This can be done by running the following command:

`git push -f`

This will push the reset to the remote repository, undoing the pull.

### Step 4: Clean Up

Finally, it is important to clean up any untracked files that may have been created by the pull. This can be done by running the following command:

`git clean -f`

This will remove any untracked files that were created by the pull.
