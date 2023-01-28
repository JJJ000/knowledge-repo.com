---
title: What is the process for saving git branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git branches can be archived by deleting them with the `git branch -d` command.
---

**Contents**

[TOC]

### Section 1 - Check Out the Branch

In order to archive a branch, you must first check out the branch you want to archive. This can be done with the following command:

`git checkout <branch_name>`

### Section 2 - Archive the Branch

Once the branch has been checked out, you can archive it with the following command:

`git archive <branch_name> --format=zip --output=<output_file.zip>`

This will create a zip file with the contents of the branch.

### Section 3 - Delete the Branch

Once the branch has been archived, you can delete the branch with the following command:

`git branch -d <branch_name>`

### Section 4 - Push the Changes

Finally, you can push the changes to the remote repository with the following command:

`git push origin --delete <branch_name>`
