---
title: Git continues to display files as changed even after they have been added to the .gitignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git will still show files as modified until they are committed and pushed to the repository.
---

**Contents**

[TOC]

### Check For Staged Files

The first step is to check if any of the files that are showing as modified have already been staged. To do this, run the command `git status` and look for any files that are listed under the "Changes to be committed" section. If any of the files that you want to ignore are listed here, they need to be un-staged before they can be ignored.

### Check the .gitignore File

The next step is to make sure that the file is included in the `.gitignore` file. If the file is not in the `.gitignore` file, it will not be ignored. Make sure that the file is included in the `.gitignore` file and that it is in the correct format.

### Remove From the Index

If the file is in the `.gitignore` file, it may still be showing as modified because it is still in the index. To remove the file from the index, run the command `git rm --cached <file>`. This will remove the file from the index and it should no longer show as modified.

### Commit the Changes

Finally, commit the changes to the `.gitignore` file and any other changes that have been made. This will ensure that the changes are applied and the file will no longer show as modified.
