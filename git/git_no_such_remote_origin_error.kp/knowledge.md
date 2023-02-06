---
title: What is the reason for git displaying the message "no such remote 'origin'" when attempting to push to origin?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git cannot find a remote repository called `origin` that has been configured for the current local repository.
---

**Contents**

[TOC]

# Cause
The cause of this error is that the remote repository, ‘origin’, has not been set up.

# Solution
To solve this issue, you need to set up the remote repository.

# Steps
1. Use the command `git remote add origin <url>` to add the remote repository.
2. Use the command `git push -u origin master` to push your changes to the remote repository.

# Conclusion
Once the remote repository is set up, you should be able to push to it without any errors.
