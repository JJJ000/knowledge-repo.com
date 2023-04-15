---
title: How can I use my preferred diff tool/ viewer to view the output of 'git diff'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the `git difftool` command to view `git diff` output with your preferred diff tool/ viewer.
---

**Contents**

[TOC]

### Setting Up Your Preferred Diff Tool
1. Find the executable path of your preferred diff tool.
2. Configure the `git config` setting for `diff.tool` to the executable path of your preferred diff tool.
3. Configure the `git config` settings for `diff.guitool` and `difftool.prompt` (optional).

### Viewing 'git diff' Output
1. Run `git difftool` in the command line.
2. Select the files you want to compare.
3. Your preferred diff tool should open the files and display the differences.
