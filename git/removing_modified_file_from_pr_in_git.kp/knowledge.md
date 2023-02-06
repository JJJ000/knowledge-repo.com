---
title: Take a modified file out of the pull request
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git reset HEAD <file>` command to remove a modified file from a pull request in Git.
---

**Contents**

[TOC]

### Reset the File

The easiest way to remove a modified file from a pull request is to reset the file. This can be done by running the following command in the terminal:

`git reset HEAD <file_name>`

This will reset the file to its original state and remove it from the pull request.

### Revert the Commit

Another way to remove a modified file from a pull request is to revert the commit that added the changes. This can be done by running the following command in the terminal:

`git revert <commit_hash>`

Reversing the commit will remove the changes from the pull request and the file will be back to its original state.

### Force Push

The last option is to force push the changes to the remote repository. This can be done by running the following command in the terminal:

`git push -f`

This will overwrite the remote repository with the local repository and the modified file will be removed from the pull request.
