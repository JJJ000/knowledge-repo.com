---
title: Error when attempting to push to the master branch of a new repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: If the repository is new and empty, there is nothing to push, so the command would fail.
---

**Contents**

[TOC]

# 1. Overview
When pushing origin master to a new repository in Git, an error can occur. This error is typically caused by a lack of permissions or incorrect configuration.

# 2. Error Message
The error message typically reads: “fatal: The current branch master has no upstream branch. To push the current branch and set the remote as upstream, use git push --set-upstream origin master”.

# 3. Causes
The error is caused by the lack of an upstream branch. This occurs when the repository is new and has not been configured to track an existing remote repository. 

# 4. Solution
The solution is to configure the repository to track an existing remote repository by running the command “git push --set-upstream origin master”. This will set up the local repository to track the remote repository and allow the user to push the changes.
