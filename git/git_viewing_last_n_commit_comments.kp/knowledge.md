---
title: View a list of remarks for my last n commits with git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use the command `git log -n N --pretty=format`%s` --no-merges` to view a list of comments of your last N commits.
---

**Contents**

[TOC]

# Using Git Log

Git log is the most common way to view a list of comments of your last N commits. To do this, you can use the following command:

`git log -n <number_of_commits>` 

This command will show you the log of your last N commits, with the most recent commit at the top. The log will also include the commit message for each commit.

# Using Git Show

Another way to view a list of comments of your last N commits is to use the `git show` command. This command will show the details of a single commit, including the commit message. To view the last N commits, you can use the following command:

`git show HEAD~<number_of_commits>`

This command will show the details of the Nth commit from the most recent one.

# Using Git For-Each-Ref

The `git for-each-ref` command is another way to view a list of comments of your last N commits. This command will display all of the commits in a given ref. To view the last N commits, you can use the following command:

`git for-each-ref --count=<number_of_commits> refs/heads/<branch_name>`

This command will show the details of the last N commits in the specified branch.

# Using Git Reflog

The `git reflog` command is another way to view a list of comments of your last N commits. This command will show the full history of the commits in a given ref. To view the last N commits, you can use the following command:

`git reflog --count=<number_of_commits>`

This command will show the details of the last N commits in the reflog.
