---
title: What causes git status to indicate that a branch is up-to-date when there are changes upstream?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git status shows that a branch is up-to-date when the local branch is synchronized with the remote branch, even if changes exist upstream.
---

**Contents**

[TOC]

### Git Status

Git status is used to check the current state of the repository and any changes that have been made. It will display the branch that is currently checked out, any changes that have been made, and any files that are staged for commit.

### Upstream Changes

When changes exist upstream, it means that someone else has committed changes to the repository that have not yet been pulled down to your local repository. Even though these changes exist, they are not yet part of your local repository and therefore, git status will still show the branch as up-to-date.

### Pulling Changes

In order to incorporate the changes from upstream, you must first pull them down to your local repository. This can be done by using the git pull command, which will fetch the changes from the remote repository and merge them into your local repository. Once this is done, git status will then show the branch as having changes.
