---
title: How can I undo a "git rm -r ." command?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git reset --hard` to revert a `git rm -r .` command.
---

**Contents**

[TOC]

### Step 1: Retrieve Deleted Files

To retrieve the files that were deleted with the `git rm -r .` command, use the following command:

```git
git checkout HEAD -- <file_name>
```

This command will restore the deleted files to the state they were in when the `git rm -r .` command was used.

### Step 2: Add Files to Staging Area

Once the deleted files have been retrieved, they must be added to the staging area to be committed. To do this, use the following command:

```git
git add <file_name>
```

This command will add the retrieved files to the staging area and make them ready to be committed.

### Step 3: Commit Changes

Once the files have been added to the staging area, they must be committed to the repository. To do this, use the following command:

```git
git commit -m "Your commit message"
```

This command will commit the changes to the repository and make them part of the history.

### Step 4: Push Changes

Finally, the changes must be pushed to the remote repository. To do this, use the following command:

```git
git push origin <branch_name>
```

This command will push the changes to the remote repository and make them available to other users.
