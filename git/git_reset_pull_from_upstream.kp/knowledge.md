---
title: Revert all modifications and fetch from the original source
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Discard all local changes and run `git pull upstream master` to pull from upstream.
---

**Contents**

[TOC]

# Discard Local Changes
1. Check the status of your local repository: `git status`
2. Discard all changes: `git reset --hard`

# Pull from Upstream
1. Set the upstream repository: `git remote add upstream <url>`
2. Fetch the upstream repository: `git fetch upstream`
3. Merge the upstream repository with your local repository: `git merge upstream/master`
