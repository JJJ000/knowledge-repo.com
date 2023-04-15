---
title: If you try to perform a 'brew update', the following files which are not being tracked by the working tree will be replaced by the merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git will refuse to merge and ask the user to resolve the conflicts manually.
---

**Contents**

[TOC]

### Resolving the Conflict

The first step in resolving the conflict is to identify which files are causing the conflict. This can be done by running `git status` to see which files are listed as being untracked or modified. Once the conflicting files have been identified, the next step is to determine which version of the conflicting files should be kept. This can be done by running `git diff` to compare the different versions of the conflicting files and decide which version should be kept. 

### Merging the Files

Once the conflicting files have been identified and the desired version has been chosen, the next step is to merge the files. This can be done by running `git merge` and specifying the files to be merged. This will create a new version of the conflicting files that contains the changes from both versions.

### Commit the Changes

Once the merge has been completed, the changes need to be committed. This can be done by running `git commit` and specifying the files to be committed. This will create a new commit that contains the changes from the merge.

### Push the Changes

The final step is to push the changes to the remote repository. This can be done by running `git push` and specifying the remote repository to which the changes should be pushed. This will push the changes to the remote repository, making them available to other users.
