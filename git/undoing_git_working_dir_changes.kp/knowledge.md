---
title: Revert all changes in the working directory, including newly created files, using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: `git reset --hard`
---

**Contents**

[TOC]

1. Discard Changes to Existing Files
-----------------------------------

To discard all changes to existing files, use the `git checkout` command. This command will restore all existing files to their last committed state.

For example, to discard all changes to all existing files, run the following command:

```
git checkout -- .
```

2. Remove Newly Added Files 
---------------------------

To remove newly added files, use the `git clean` command. This command will delete all untracked files and directories.

For example, to delete all untracked files and directories, run the following command:

```
git clean -df
```

3. Revert Committed Changes
---------------------------

To revert committed changes, use the `git revert` command. This command will undo the changes made in a particular commit.

For example, to revert the changes made in a particular commit, run the following command:

```
git revert <commit_hash>
```

4. Reset the Working Directory
------------------------------

To reset the working directory to its last committed state, use the `git reset` command. This command will reset the working directory to the last committed state.

For example, to reset the working directory to its last committed state, run the following command:

```
git reset --hard
```
