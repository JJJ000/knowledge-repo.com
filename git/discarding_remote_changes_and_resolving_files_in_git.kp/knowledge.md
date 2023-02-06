---
title: What is the best way to undo remote changes and mark a file as "resolved"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To discard remote changes and mark a file as `resolved` in Git, use the `git checkout --ours/--theirs` command.
---

**Contents**

[TOC]

# Discard Remote Changes
1. Fetch the latest version of the repository: `git fetch`.
2. Checkout the branch you want to discard the changes for: `git checkout <branch-name>`.
3. Reset the branch to the remote version: `git reset --hard origin/<branch-name>`.

# Mark File as "Resolved"
1. Checkout the branch you want to mark the file as resolved for: `git checkout <branch-name>`.
2. Add the file to the staging area: `git add <file-name>`.
3. Commit the file: `git commit -m "Marked <file-name> as resolved"`.
