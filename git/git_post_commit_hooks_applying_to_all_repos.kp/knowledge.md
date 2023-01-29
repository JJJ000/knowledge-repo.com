---
title: Adding a git post-commit hook to all existing and new repositories
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Create a global git template directory and add the post-commit hook to the template directory so that it will be applied to all current and future repositories.
---

**Contents**

[TOC]

### Overview

Git post-commit hooks are scripts that run after a successful commit. They can be used to automate tasks such as running tests, sending notifications, or performing other operations. Applying a git post-commit hook to all current and future repositories requires setting up the hook in the global git configuration.

### Setting Up the Hook

1. Create the hook script and save it to a file.
2. Set the executable permissions on the file.
3. Configure the global git configuration by running `git config --global core.hooksPath <path to hook file>`.

### Applying to Existing Repositories

1. Change into each existing repository directory.
2. Run `git init` to reinitialize the repository.

### Applying to Future Repositories

The hook will automatically be applied to all future repositories when they are initialized.
