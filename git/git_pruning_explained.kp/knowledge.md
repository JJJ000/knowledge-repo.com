---
title: How do git remote prune, git prune, and git fetch --prune differ?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git remote prune removes stale references from a remote repository, git prune removes objects that are no longer pointed to by any object in any reachable branch, and git fetch --prune updates the local repository with the remote repository, while also pruning any stale references.
---

**Contents**

[TOC]

**Git Remote Prune** 
Git remote prune is used to delete branches that have been deleted from the remote repository, but still exist locally. This command will only remove references to remote branches that no longer exist. 

**Git Prune** 
Git prune is used to delete local references to remote branches that have been deleted from the remote repository. This command will delete any local references to branches that no longer exist on the remote repository.

**Git Fetch --Prune**
Git fetch --prune is used to fetch new remote branches and delete local references to branches that have been deleted from the remote repository. This command will fetch new branches from the remote repository and delete any local references to branches that no longer exist on the remote repository.

**Git Fetch**
Git fetch is used to fetch new remote branches and update local references to branches that have been updated on the remote repository. This command will fetch new branches from the remote repository and update any local references to branches that have been updated on the remote repository.
