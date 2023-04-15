---
title: Fetch the latest changes from the original github repository and incorporate them into the forked github repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Fetch and merge changes from the original repository into your forked repository.
---

**Contents**

[TOC]

### Step 1: Set Up Remote

1. Open the terminal and change the current working directory to your local project.
2. List your current configured remote repository using `git remote -v`.
3. If the original repository is not listed, you will need to add it as a remote repository.
4. Use the `git remote add` command to add the original repository as a remote.

### Step 2: Fetch Updates

1. Fetch the branches and their respective commits from the upstream repository.
2. Use the `git fetch` command to fetch the branches and commits from the upstream repository.

### Step 3: Merge Updates

1. Use the `git merge` command to merge the remote changes into your local repository.
2. Confirm the merge commit to finalize the merge.

### Step 4: Push Updates

1. Push the changes in your local repository to GitHub.
2. Use the `git push` command to push the changes to your forked GitHub repository.
