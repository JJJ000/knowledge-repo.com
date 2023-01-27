---
title: What is the process for altering the author of a single commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git commit --amend --author=`Author Name <email@address.com>`` to change the author of a single commit.
---

**Contents**

[TOC]

#1. Find the Commit

The first step to changing the commit author for a single commit in Git is to find the commit you want to change. You can use the `git log` command to view all the commits in your repository. This will list all the commits, with their commit hashes and authors. You can then find the commit you want to change and copy its commit hash.

#2. Change the Author

Once you have the commit hash, you can use the `git rebase` command to change the author of the commit. The command will look something like this:

`git rebase -i <commit-hash>^ --committer-date-is-author-date --no-edit`

This command will open an interactive rebase editor, where you can change the author of the commit. You can then save and close the editor, and the commit author will be changed.

#3. Push the Changes

The next step is to push the changes to the remote repository. You can do this with the `git push` command. This will push the changes to the remote repository, and the commit author will be changed.

#4. Clean Up

The final step is to clean up any temporary files that were created during the rebase process. You can do this with the `git rebase --abort` command. This will remove any temporary files and ensure that your repository is in a clean state.
