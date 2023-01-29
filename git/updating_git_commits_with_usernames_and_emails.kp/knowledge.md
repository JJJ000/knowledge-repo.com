---
title: Replace the author information of the previous commit in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git commit --amend --reset-author` to rewrite the previous commit usernames and emails.
---

**Contents**

[TOC]

### Using `git filter-branch`

1. Create a backup of your repository:

`git clone --bare <old-repository-url> <backup-directory>`

2. Checkout a new branch from the master branch:

`git checkout -b <new-branch>`

3. Rewrite the commits with the new username and email address:

`git filter-branch --env-filter 'if [ "$GIT_COMMITTER_EMAIL" = "<old-email>" ]; then
    export GIT_COMMITTER_NAME="<new-name>";
    export GIT_COMMITTER_EMAIL="<new-email>";
fi' -- --all`

4. Push the new branch to the remote repository:

`git push --force --set-upstream origin <new-branch>`

### Using `git rebase`

1. Create a backup of your repository:

`git clone --bare <old-repository-url> <backup-directory>`

2. Checkout a new branch from the master branch:

`git checkout -b <new-branch>`

3. Rewrite the commits with the new username and email address:

`git rebase --env-filter 'if [ "$GIT_COMMITTER_EMAIL" = "<old-email>" ]; then
    export GIT_COMMITTER_NAME="<new-name>";
    export GIT_COMMITTER_EMAIL="<new-email>";
fi' -- --all`

4. Push the new branch to the remote repository:

`git push --force --set-upstream origin <new-branch>`
