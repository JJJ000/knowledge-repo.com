---
title: What is the frequency of git updating the list of remote branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git refreshes the list of remote branches when running the command `git fetch`.
---

**Contents**

[TOC]

1. Fetching Remote Branches
--------------------------------
Git refreshes the list of remote branches when it performs a Fetch operation. This operation is initiated either manually or automatically.

2. Manual Fetch
----------------
A manual Fetch operation can be initiated by using the command `git fetch`, or by using the `git pull` command with the `--all` option. This will retrieve the list of all remote branches and store them locally.

3. Automatic Fetch
-------------------
Git can also be configured to automatically fetch remote branches. This can be done by using the `git config` command with the `--global` option. This will cause Git to periodically fetch the list of remote branches and store them locally.

4. Verifying Remote Branches
-----------------------------
Once the list of remote branches has been fetched, it can be verified by using the `git branch -r` command. This will display a list of all the remote branches that have been fetched.
