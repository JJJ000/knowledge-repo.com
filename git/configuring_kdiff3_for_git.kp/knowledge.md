---
title: What steps do I need to take to set kdiff3 as the merge and diff tool for git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git config --global merge.tool kdiff3` and `git config --global diff.tool kdiff3` to configure KDiff3 as the merge and diff tool for Git.
---

**Contents**

[TOC]

### Setting Up KDiff3 as Merge Tool
1. Install KDiff3 on your system.
2. Set up the configuration in your `.gitconfig` file:
```git
[merge]
	tool = kdiff3
[mergetool "kdiff3"]
	path = /usr/bin/kdiff3
	trustExitCode = false
```
3. Run the command `git mergetool` to invoke the merge tool.

### Setting Up KDiff3 as Diff Tool
1. Install KDiff3 on your system.
2. Set up the configuration in your `.gitconfig` file:
```git
[diff]
	tool = kdiff3
[difftool "kdiff3"]
	path = /usr/bin/kdiff3
	trustExitCode = false
```
3. Run the command `git difftool` to invoke the diff tool.
