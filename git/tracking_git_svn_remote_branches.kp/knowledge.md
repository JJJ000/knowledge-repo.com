---
title: What is the process for informing git-svn of a remote branch that was created after I retrieved the repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git svn fetch` to update your local repo with the remote branch.
---

**Contents**

[TOC]

1. __Fetch the Remote Branch__

Run the following command to fetch the new remote branch:

`git svn fetch --all`

2. __Check Out the Remote Branch__

Check out the new remote branch by running the following command:

`git checkout -b <branch-name> <remote-name>/<branch-name>`

3. __Track the Remote Branch__

Track the new remote branch by running the following command:

`git branch --track <local-name> <remote-name>/<branch-name>`

4. __Push the Local Branch__

Push the local branch to the remote branch by running the following command:

`git push <remote-name> <local-name>`
