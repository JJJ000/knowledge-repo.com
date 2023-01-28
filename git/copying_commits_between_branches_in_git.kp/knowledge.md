---
title: What is the process for transferring commits from one branch to another?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To copy commits from one branch to another in Git, use the `git cherry-pick <commit-hash>` command.
---

**Contents**

[TOC]

### Preparing to Copy Commits
1. Check out the source branch: `git checkout source_branch`
2. Check out the destination branch: `git checkout destination_branch`

### Copying Commits
1. Cherry-pick the commits you want to copy: `git cherry-pick <commit-hash>`
2. Repeat step 1 for each commit you want to copy.

### Pushing Commits
1. Push the commits to the destination branch: `git push origin destination_branch`

### Verifying Changes
1. Verify the changes have been copied to the destination branch: `git log --oneline --graph --decorate --all`
