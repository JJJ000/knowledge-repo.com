---
title: What command do I use to view changes made to a specific branch using git log?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git log <branch-name>` to see changes only for a specific branch.
---

**Contents**

[TOC]

### Syntax

`git log <branch_name>`

### Description

The `git log` command allows you to view the history of commits for a specific branch. This command can be used to view the changes made to a specific branch over time.

### Options

You can also add additional options to the command to refine the output. For example, you can add the `--oneline` option to show each commit on one line or the `--graph` option to show a graph of the commits.

### Examples

To view the commits for the `master` branch, you can run the following command:

`git log master`
