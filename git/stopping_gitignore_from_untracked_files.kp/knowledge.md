---
title: How can I prevent .gitignore from showing up in the list of untracked files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can exclude the .gitignore file from being tracked by running `git update-index --skip-worktree .gitignore`.
---

**Contents**

[TOC]

### Add .gitignore to .git/info/exclude

By adding .gitignore to the .git/info/exclude file, you can tell Git to ignore it when it is listed in the list of untracked files. This will ensure that .gitignore is not included in the list of untracked files.

### Use git update-index

You can also use the git update-index command to tell Git to not track .gitignore. This command can be used to tell Git to ignore certain files and directories.

### Use git config

You can also use the git config command to tell Git to ignore certain files and directories. This command can be used to add entries to the .git/info/exclude file.

### Commit .gitignore

Finally, you can commit .gitignore to the repository. This will ensure that .gitignore is tracked and will no longer appear in the list of untracked files.
