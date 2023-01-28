---
title: What files are in my local git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To list files in a local Git repo, use the `git ls-files` command.
---

**Contents**

[TOC]

1. `.git/` Folder
   - `COMMIT_EDITMSG`
   - `config`
   - `description`
   - `HEAD`
   - `hooks/`
   - `index`
   - `info/`
   - `logs/`
   - `objects/`
   - `refs/`

2. Working Directory
   - All tracked and untracked files in the directory.

3. Staging Area
   - Files that have been added to the staging area.

4. Ignored Files
   - Files that are being ignored by Git.
