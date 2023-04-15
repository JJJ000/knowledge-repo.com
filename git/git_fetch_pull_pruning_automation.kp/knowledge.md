---
title: Perform an automated pruning of branches with a git fetch or pull
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git fetch or pull does not automatically prune branches.
---

**Contents**

[TOC]

### Git Fetch

Git fetch is used to download objects and references from a remote repository into the local repository. It does not merge the downloaded content into the local repository. Instead, it stores the objects and references in the local repository's FETCH_HEAD file.

### Automatic Prune

When using Git fetch, an automatic prune can be enabled. This feature will delete any remote-tracking branches that no longer exist in the remote repository. This helps to keep the local repository clean and up-to-date. 

### Benefits

Enabling automatic prune with Git fetch can help to reduce clutter in the local repository. It also ensures that the local repository is up-to-date with the remote repository, which can help prevent conflicts during future merges and pulls.

### Drawbacks

One potential drawback of using automatic prune with Git fetch is that it can delete branches that are still needed. This can be avoided by using the --prune-tags flag, which will only delete remote-tracking branches that have been deleted from the remote repository.
