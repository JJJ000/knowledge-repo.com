---
title: What is the process for deleting files with the description "old mode 100755 new mode 100644" from unstaged changes in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git checkout -- <file>` to discard the changes and reset the file to its previous state.
---

**Contents**

[TOC]

1. **Check the File Status:**
Before attempting to remove the files, it is important to check the status of the files. This can be done by running the command `git status` to check the files that are currently unstaged and need to be addressed.

2. **Check the File Contents:**
If the files in question are listed in the unstaged changes, it is important to check the contents of the files to ensure they are the correct files that need to be removed. This can be done by running the command `git show` to view the contents of the file.

3. **Remove the Files:**
Once the files have been identified, they can be removed from the unstaged changes by running the command `git reset --hard`. This will remove the files from the unstaged changes and reset the repository to its previous state.

4. **Verify Changes:**
Finally, it is important to verify that the files have been removed from the unstaged changes. This can be done by running the command `git status` again to check that the files are no longer listed in the unstaged changes.
