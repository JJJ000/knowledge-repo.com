---
title: Verifying for any unsaved changes or untracked files with git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git status` to check for a dirty index or untracked files.
---

**Contents**

[TOC]

1. Checking for a Dirty Index

- To check for a dirty index, use the `git status` command. This will show a list of files that have been modified, added, or deleted since the last commit. If any of these files are in the index, they will be marked as 'Changes not staged for commit'. 

2. Checking for Untracked Files

- To check for untracked files, use the `git ls-files --other --exclude-standard` command. This will list all untracked files that are not in the .gitignore file. If any files are listed, they will need to be added to the index before they can be committed. 

3. Adding Files to the Index

- To add files to the index, use the `git add <file>` command. This will add the specified file to the index and make it ready to be committed. 

4. Committing the Changes

- To commit the changes, use the `git commit -m "message"` command. This will commit the changes in the index with the specified message. Once the changes are committed, they will be visible in the Git log.
