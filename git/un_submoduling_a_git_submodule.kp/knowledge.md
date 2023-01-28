---
title: What is the process for removing a git submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git submodule deinit <submodule name>` followed by `git rm <submodule name>` and finally `git commit -m `Removed submodule <submodule name>``.
---

**Contents**

[TOC]

### Remove Submodule from .gitmodules
1. Open the .gitmodules file in the root directory of your repository.
2. Locate the submodule you wish to remove, and delete the corresponding section.
3. Save and close the .gitmodules file.

### Remove Submodule from .git/config
1. Open the .git/config file in the root directory of your repository.
2. Locate the submodule you wish to remove, and delete the corresponding section.
3. Save and close the .git/config file.

### Remove Submodule from Working Tree
1. Change to the root directory of your repository.
2. Run the command `git rm --cached <submodule_name>` to remove the submodule from the working tree.

### Commit Changes
1. Run the command `git commit -m "Removed submodule <submodule_name>"` to commit the changes.
