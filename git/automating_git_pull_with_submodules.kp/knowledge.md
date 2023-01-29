---
title: Can git pull be configured to automatically update submodules?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, by setting the `--recurse-submodules` flag when running `git pull`.
---

**Contents**

[TOC]

### Option 1: Using the `--recurse-submodules` Flag

The `--recurse-submodules` flag can be used when pulling from a remote repository to update the submodules. For example, the command `git pull --recurse-submodules` will pull from the remote repository and update all submodules.

### Option 2: Setting the `submodule.recurse` Configuration Option

The `submodule.recurse` configuration option can be set to true to enable recursive updating of submodules. This can be done by running `git config --global submodule.recurse true`. This will cause all subsequent `git pull` commands to update the submodules.

### Option 3: Using the `git submodule update` Command

The `git submodule update` command can be used to update all submodules in the repository. This command can be run manually or can be added to a script that is run after each `git pull`.

### Option 4: Using a Post-Checkout Hook

A post-checkout hook can be created to update the submodules after each `git pull`. The post-checkout hook is a script that is run after each `git pull` and can be configured to update the submodules.
