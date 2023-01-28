---
title: Pushing code to two remote repositories using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can push code to two remotes by pushing to each remote separately.
---

**Contents**

[TOC]

### Option 1: Aliasing

One way to push code to two remotes is by aliasing one remote as the other. This can be done by running the command `git remote add <alias> <url>`. This will create a local alias for the remote URL. When pushing code, the command `git push <alias>` can then be used to push the code to both remotes.

### Option 2: Running Push Twice

Another option is to simply run the `git push` command twice, once for each remote. This can be done by specifying the remote name in the command, like so: `git push <remote-name> <branch-name>`.

### Option 3: Using a Script

A third option is to create a script to automate the process. This script can be set up to run the `git push` command for both remotes automatically. This can be done by creating a bash script that runs the command for each remote.

### Option 4: Using Git Hooks

A fourth option is to use Git hooks. Git hooks are scripts that run automatically when certain Git commands are executed. By creating a pre-push hook, the script can be set up to run the `git push` command for both remotes whenever the `git push` command is executed.
