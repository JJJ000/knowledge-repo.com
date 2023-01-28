---
title: Changing the name of a branch in github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To rename a branch in GitHub, use the `Rename` button on the branch`s page.
---

**Contents**

[TOC]

### Renaming a Branch in GitHub

### Step 1: Rename Locally
1. Open your terminal and navigate to the local repository that contains the branch you want to rename.
2. Run the command `git branch -m <oldname> <newname>` to rename the branch.

### Step 2: Push the Changes to GitHub
1. Run the command `git push origin :<oldname> <newname>` to delete the old branch and push the new branch to GitHub.

### Step 3: Verify the Changes
1. Go to your repository in GitHub and verify that the branch has been renamed.
