---
title: Remove file from "git diff"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git diff -- . `(exclude)filename`` command to exclude a file from the git diff output.
---

**Contents**

[TOC]

### Add .gitignore File

The first step to excluding files from `git diff` is to add a `.gitignore` file to the repository. This file should contain a list of files, directories, and patterns that should be excluded from version control.

### Configure git

The second step is to configure git to ignore certain files. This can be done by running the `git config` command with the `--global` flag. This will add a setting to the global configuration file, which will apply to all repositories.

### Exclude Files

The third step is to exclude files from the repository. This can be done by running the `git rm` command with the `--cached` flag. This will remove the file from the repository, but will not delete it from the working directory.

### Commit Changes

The final step is to commit the changes. This can be done with the `git commit` command. This will save the changes to the repository, and the excluded files will no longer be included in the `git diff` output.
