---
title: What is the best way to proceed or abort the rebase that is currently in progress if I am unable to commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To proceed, run `git rebase --continue`, to abort, run `git rebase --abort`.
---

**Contents**

[TOC]

# Stopping Rebase

1. To stop a rebase, you can use the `git rebase --abort` command. This command will abort the current rebase and return the repository to the state before the rebase was initiated.

2. If you have made any changes during the rebase, you will be prompted to save them before the rebase is aborted. If you do not want to save the changes, you can use the `--no-edit` option to abort the rebase without saving the changes.

# Proceeding with Rebase

1. To proceed with the rebase, you can use the `git rebase --continue` command. This command will continue the rebase process, applying the next patch in the sequence.

2. If there are any conflicts between the patch and the current state of the repository, you will be prompted to resolve them before the rebase can continue. Once the conflicts are resolved, you can use the `--continue` command again to continue the rebase process.
