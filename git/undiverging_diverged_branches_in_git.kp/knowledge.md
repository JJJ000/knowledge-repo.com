---
title: How can I bring the 'master branch' and 'origin/master' back into alignment?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the `git reset --hard origin/master` command to reset your master branch to match the origin/master branch.
---

**Contents**

[TOC]

### Step 1: Fetch from Remote

Before attempting to bring the local and remote branches back in sync, it is important to make sure that the local copy of the remote branch is up-to-date. This can be done by running the command:

`git fetch origin`

### Step 2: Checkout Local Branch

Next, the local branch needs to be checked out. This can be done by running the command:

`git checkout master`

### Step 3: Rebase Local Branch

Once the local branch is checked out, it can be rebased against the remote branch. This can be done by running the command:

`git rebase origin/master`

### Step 4: Push to Remote

Finally, the local branch can be pushed to the remote branch. This can be done by running the command:

`git push origin master`
