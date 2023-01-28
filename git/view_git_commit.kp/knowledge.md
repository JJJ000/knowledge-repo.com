---
title: Look at a particular git commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can view a specific Git commit by using the command `git show <commit-hash>`.
---

**Contents**

[TOC]

### Viewing a Git Commit

Git commits are snapshots of a repository at a certain point in time. Viewing a commit allows you to see the changes that were made to the repository at that particular point. 

### Viewing a Commit Using the Command Line

The most common way to view a specific Git commit is to use the `git log` command. This command will display a list of all commits in the repository, along with their commit messages, authors, and dates. To view a specific commit, you can use the `git show` command followed by the commit hash. This will display the commit message, author, and date, as well as a diff of all the changes that were made in that commit. 

### Viewing a Commit Using a GUI

Most graphical user interfaces (GUIs) for Git (such as GitHub Desktop) will allow you to view a specific commit. This can usually be done by selecting the commit from a list of commits, or by entering the commit hash. The GUI will then display the commit message, author, date, and a diff of all the changes that were made in that commit.

### Viewing a Commit on GitHub

If the repository is hosted on GitHub, then you can view the commit directly in the web browser. Simply navigate to the repository, and then select the "Commits" tab. This will display a list of all commits in the repository, and you can select a specific commit to view its message, author, date, and diff.
