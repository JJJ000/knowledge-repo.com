---
title: What is the process for altering the timestamp of an existing commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git commit --amend --date=`<new date>`` to change the timestamp of an old commit in Git.
---

**Contents**

[TOC]

#1 Using Amend

The `git commit --amend` command can be used to change the timestamp of an old commit. This command allows the user to modify the most recent commit by adding changes to the commit or modifying the commit message. The user can also modify the timestamp of the commit by passing the `--date` option to the command.

#2 Using Filter-Branch

The `git filter-branch` command can also be used to change the timestamp of an old commit. This command allows the user to rewrite the entire history of a branch by applying a set of filters to each commit. The user can use the `--env-filter` option to modify the environment variables associated with each commit, including the `GIT_AUTHOR_DATE` and `GIT_COMMITTER_DATE` variables which are used to set the timestamp of the commit.

#3 Using Rebase

The `git rebase` command can also be used to change the timestamp of an old commit. This command allows the user to rewrite the history of a branch by replaying a set of commits on top of a different commit. The user can use the `--committer-date-is-author-date` option to ensure that the timestamp of each commit is set to the author's timestamp instead of the committer's timestamp. This can be used to modify the timestamp of an old commit.

#4 Using Reset

The `git reset` command can also be used to change the timestamp of an old commit. This command allows the user to reset the HEAD of a branch to a different commit. The user can use the `--soft` and `--date` options to reset the HEAD to an old commit and modify the timestamp of that commit.
