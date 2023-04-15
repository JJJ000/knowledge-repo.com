---
title: What is the best way to set up git so that it uses rebase as the default pull method for all my repositories?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git config --global pull.rebase true` to make Git pull use rebase by default for all your repositories.
---

**Contents**

[TOC]

### Setting Up Global Config
1. Open the Git configuration file by running `git config --global --edit`
2. Add the following line to the configuration file: `pull.rebase = true`
3. Save the configuration file and close it.

### Setting Up Local Config
1. Change directory to the local repository you want to use rebase by default.
2. Open the Git configuration file by running `git config --local --edit`
3. Add the following line to the configuration file: `pull.rebase = true`
4. Save the configuration file and close it.

### Verifying the Configuration
1. Run `git config --list` to view all the configuration settings for the repository.
2. Look for the line `pull.rebase = true` to verify the configuration was set correctly.
