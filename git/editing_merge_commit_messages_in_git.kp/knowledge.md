---
title: How to modify the message of a git merge commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To edit/reword a merge commit`s message, use the command `git commit --amend -m ` followed by the new message.
---

**Contents**

[TOC]

## Using the Command Line
1. Check out the branch you wish to edit the merge commit on.
   ```
   git checkout <branch-name>
   ```
2. Use the interactive rebase command to edit the merge commit.
   ```
   git rebase -i <parent-of-merge-commit>
   ```
3. In the editor that opens, replace `pick` with `reword` for the merge commit you wish to edit.
4. Save and close the editor. The rebase will continue, and you will be able to edit the merge commit message.

## Using a GUI
1. Launch the GUI of your choice.
2. Check out the branch you wish to edit the merge commit on.
3. Find the merge commit you wish to edit.
4. Right-click the merge commit and select "Reword Commit".
5. Edit the merge commit message and save your changes.
