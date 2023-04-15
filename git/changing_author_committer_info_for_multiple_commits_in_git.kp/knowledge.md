---
title: What is the process for altering the author and committer name/email for multiple commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git rebase -i HEAD~<number of commits>` and then use the `reword` command to change the author and committer for each commit.
---

**Contents**

[TOC]

### Section 1 - Using git rebase

1. Run `git rebase -i HEAD~<number of commits>` to open an interactive rebase session.
2. Change `pick` to `reword` for each commit you want to change the author/committer name/email.
3. When prompted, enter the new author/committer name/email.
4. After all the commits have been reworded, run `git rebase --continue` to finish the rebase.

### Section 2 - Using git filter-branch

1. Run `git filter-branch --env-filter 'if [ "$GIT_AUTHOR_EMAIL" = "<old email>" ]; then GIT_AUTHOR_EMAIL="<new email>"; GIT_AUTHOR_NAME="<new name>"; fi; if [ "$GIT_COMMITTER_EMAIL" = "<old email>" ]; then GIT_COMMITTER_EMAIL="<new email>"; GIT_COMMITTER_NAME="<new name>"; fi'`
2. After the command has finished running, verify that the author/committer name/email has been changed by running `git log`.

### Section 3 - Pushing the changes

1. Run `git push origin <branch name> --force` to push the changes to the remote repository.

### Section 4 - Cleaning up

1. Run `git for-each-ref --format="%(refname)" refs/original/ | xargs -n 1 git update-ref -d` to delete the backup references created by the filter-branch command.
