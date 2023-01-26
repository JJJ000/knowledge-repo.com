---
title: What is the process for changing the message of an already committed but not yet pushed commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Use the `git commit --amend` command to modify existing, unpushed commit messages in Git.
---

**Contents**

[TOC]

### Commit the Changes

Before modifying an existing commit message, you must first commit the changes you have made. To do this, use the `git commit` command.

### Amend the Commit Message

Once your changes have been committed, you can modify the commit message by using the `git commit --amend` command. This will open up an editor window where you can modify the commit message.

### Push the Commit

Once you have modified the commit message, you will need to push the commit to the remote repository. To do this, use the `git push` command.

### Confirm the Changes

Finally, you can confirm the changes have been made by running the `git log` command. This will show the updated commit message in the log.
