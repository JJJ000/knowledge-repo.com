---
title: What is the process for cherry-picking only modifications to specific files using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git cherry-pick <commit> -- <filename>` command to cherry-pick only changes to certain files.
---

**Contents**

[TOC]

1. Find the Commit
First, you need to find the commit that contains the changes you want to cherry-pick. You can do this by searching for the commit in your version control system (e.g. Git).

2. Checkout the Commit
Once you have identified the commit, you need to checkout the commit to your local repository. This can be done by using the `git checkout` command with the commit's SHA-1 hash.

3. Cherry-Pick the Changes
Once you have the commit checked out locally, you can use the `git cherry-pick` command to pick only the changes to certain files. You can specify the files you want to cherry-pick by using the `--path` or `--name-only` flags.

4. Push the Changes
Finally, once you have cherry-picked the changes to the files you wanted, you can push the changes to your remote repository using the `git push` command.
