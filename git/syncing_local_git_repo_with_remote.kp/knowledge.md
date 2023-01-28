---
title: Matching a local git repository with a remote one
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To synchronize a local Git repository with a remote one, use the git pull and git push commands.
---

**Contents**

[TOC]

1. Add the Remote Repository
--------------------------------

Begin by adding the remote repository to your local Git repository. This can be done by running the command `git remote add <remote-name> <remote-url>`. The `<remote-name>` should be a name you assign to the remote repository and `<remote-url>` should be the URL of the remote repository.

2. Fetch the Remote Repository
-------------------------------

Once the remote repository is added, you can fetch the remote repository by running the command `git fetch <remote-name>`. This will download all the changes from the remote repository and store them as a separate branch in your local repository.

3. Merge the Remote Repository
-------------------------------

Once the remote repository has been fetched, you can merge the changes from the remote repository into your local repository. This can be done by running the command `git merge <remote-name>/<branch-name>`. This will merge the changes from the remote repository into the specified branch in your local repository.

4. Push to the Remote Repository
---------------------------------

Once the changes from the remote repository have been merged into your local repository, you can push the changes to the remote repository. This can be done by running the command `git push <remote-name> <branch-name>`. This will push the changes from your local repository to the remote repository.
