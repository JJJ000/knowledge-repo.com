---
title: Git will not initiate, synchronize, or update any new submodules
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git will not init/sync/update new submodules unless they are explicitly added to the repository.
---

**Contents**

[TOC]

### Initializing Submodules

Git will initialize a new submodule when a repository is cloned. This can be done by running the `git submodule init` command.

### Syncing Submodules

Git will sync a submodule when the repository is updated. This can be done by running the `git submodule sync` command.

### Updating Submodules

Git will update a submodule when the repository is updated. This can be done by running the `git submodule update` command.

### Deleting Submodules

Git will delete a submodule when the repository is updated. This can be done by running the `git submodule deinit` command.
