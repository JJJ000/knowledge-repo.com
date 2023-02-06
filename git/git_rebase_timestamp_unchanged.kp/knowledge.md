---
title: Git rebase without altering commit dates
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, it is possible to rebase without changing commit timestamps by using the `--preserve-merges` flag.
---

**Contents**

[TOC]

# Using the --no-ff Option

When using git rebase, you can use the `--no-ff` option to prevent the commit timestamps from being changed. This option will keep all the original timestamps of the commits intact.

# Using the --preserve-merges Option

Another option is to use the `--preserve-merges` option when running git rebase. This option will keep all the original timestamps of the commits intact, as well as any merge commits.

# Using the --rebase-merges Option

The `--rebase-merges` option can also be used when running git rebase. This option will keep all the original timestamps of the commits intact, as well as any merge commits, while also allowing the commits to be replayed.

# Using the --no-commit Option

Finally, the `--no-commit` option can be used when running git rebase. This option will prevent any commits from being created, thus preserving all the original timestamps of the commits.
