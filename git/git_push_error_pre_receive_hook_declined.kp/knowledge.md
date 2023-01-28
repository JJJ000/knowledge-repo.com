---
title: Error encountered when attempting to push changes to a git repository -- pre-receive hook declined
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The pre-receive hook declined the push, meaning the changes were not accepted into the repository.
---

**Contents**

[TOC]

### Overview
When attempting to push changes to a Git repository, the pre-receive hook can decline the push. This is a type of error that occurs when the pre-receive hook on the remote repository is configured to reject certain types of changes or commits.

### Causes
The pre-receive hook is a script that runs on the remote repository when changes are pushed to it. It is typically used to perform checks on the pushed changes, such as verifying that the commit message matches a certain format or that certain files have not been changed. If the pre-receive hook detects a violation of its configured rules, it will reject the push and return an error.

### Solutions
If you encounter a pre-receive hook error, the first step is to identify the cause of the error. This can usually be done by examining the output of the pre-receive hook script. Once the cause of the error is identified, it can be addressed by either changing the configuration of the pre-receive hook or by changing the pushed changes to comply with the hook's requirements.
