---
title: What is the process for inserting a commit between two existing commits in the past?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git rebase -i <earlier commit>` to open the interactive rebase editor, then add a new commit and save the changes.
---

**Contents**

[TOC]

# Section 1: Find the Commits

In order to inject a commit between two arbitrary commits in the past, the first step is to find the two commits. This can be done using the `git log` command.

# Section 2: Create a New Branch

Once the two commits have been identified, the next step is to create a new branch off of the commit before the one that you want to inject the commit between. This can be done with the `git checkout -b` command.

# Section 3: Create the Commit

Once the new branch has been created, the next step is to create the commit. This can be done with the `git commit` command.

# Section 4: Merge the Branch

Once the commit has been created, the final step is to merge the branch back into the main branch. This can be done with the `git merge` command.
