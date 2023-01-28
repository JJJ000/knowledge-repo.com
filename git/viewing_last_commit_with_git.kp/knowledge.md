---
title: View my last commit using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can view your last commit by running the command `git log -1` in the terminal.
---

**Contents**

[TOC]

### Using the `git log` Command

The `git log` command is the best way to view a list of all the commits in a repository. To view the most recent commit, you can use the `git log -1` command. This will show you the details of the last commit, including the author, date, and commit message.

### Using the `git show` Command

The `git show` command can also be used to view the details of a specific commit. To view the details of the last commit, you can use the `git show HEAD` command. This will show you the same information as the `git log -1` command, but it will also show the changes that were made in the commit.

### Using the `git reflog` Command

The `git reflog` command can be used to view a list of recent commits, including those that have been reverted or amended. To view the details of the last commit, you can use the `git reflog HEAD` command. This will show you the same information as the `git log -1` and `git show HEAD` commands, but it will also show the commit that was amended or reverted.

### Using the GitHub Web Interface

If you are using GitHub, you can also view the details of your last commit in the web interface. On the main page of the repository, click on the "Commits" tab. This will show you a list of all the commits in the repository, with the most recent commit at the top. Clicking on the commit will show you the details of the commit, including the author, date, and commit message.
