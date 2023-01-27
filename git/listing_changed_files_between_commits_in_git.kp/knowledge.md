---
title: What is the command to show only the filenames that were modified between two commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the `git diff --name-only <commit1> <commit2>` command.
---

**Contents**

[TOC]

### Prepare the Repository
1. Pull the latest changes from the remote repository:
   ```git pull origin master```
2. Checkout the commit before the one you want to compare against:
   ```git checkout <commit-hash-before>```

### List the Changed Files
1. Use the command `git diff --name-only <commit-hash-before> <commit-hash-after>` to list the files that have changed between the two commits

### Filter the Output
1. If needed, you can filter the output of the command with `grep` to only show the file names:
   ```git diff --name-only <commit-hash-before> <commit-hash-after> | grep -E '\.(txt|py)$'```

### Save the Output
1. To save the output of the command to a file, use the `tee` command:
   ```git diff --name-only <commit-hash-before> <commit-hash-after> | grep -E '\.(txt|py)$' | tee changed_files.txt```
