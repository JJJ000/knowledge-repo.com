---
title: What is the process for combining two commits that are not directly next to each other?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the interactive rebase tool (git rebase -i) to squash non-consecutive commits.
---

**Contents**

[TOC]

**1. Checkout the Commit You Want to Squash**

First, check out the commit you want to squash. To do this, you can use the `git checkout` command. For example, if you want to squash the last two commits, you can use `git checkout HEAD~2`. This will check out the commit two steps before the current HEAD.

**2. Rebase onto the Commit You Want to Squash**

Next, use the `git rebase` command to rebase onto the commit you want to squash. For example, if you want to squash the last two commits, you can use `git rebase -i HEAD~2`. This will open up an interactive rebase session which will allow you to edit the commits you want to squash.

**3. Squash the Commits**

In the interactive rebase session, you will see a list of the commits you want to squash. You can then use the `squash` command to squash the commits into one. This will combine the commits into a single commit.

**4. Finish the Rebase**

Once you have squashed the commits, you can finish the rebase. To do this, you can use the `git rebase --continue` command. This will finish the rebase and apply the squashed commits to your branch.
