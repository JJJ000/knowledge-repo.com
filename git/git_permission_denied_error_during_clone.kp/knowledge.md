---
title: When attempting to clone a git repository, an error occurred due to a lack of permission 'git permission denied (publickey) fatal - could not read from remote repository.'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The error indicates that the SSH key used to authenticate the clone is not valid.
---

**Contents**

[TOC]

# Section 1: Overview
Git is a distributed version control system used for tracking changes in source code during software development. It is commonly used for collaboration and source code management. When using Git, it is possible to encounter the error "Permission denied (publickey) fatal - Could not read from remote repository" while cloning a repository. This error occurs when the user does not have the correct permissions to access the remote repository. 

# Section 2: Causes
This error can occur due to a few different reasons, such as:

1. Incorrect SSH Key: The user may not have the correct SSH key associated with their account, or the key may not be in the correct format.

2. Incorrect Permissions: The user may not have the correct permissions to access the remote repository.

3. Firewall: The user's connection may be blocked by a firewall.

# Section 3: Solutions
To resolve this error, the user should try the following solutions:

1. Check SSH Key: The user should check that their SSH key is in the correct format and associated with their account.

2. Check Permissions: The user should check that they have the correct permissions to access the remote repository.

3. Check Firewall: The user should check that their connection is not being blocked by a firewall.

# Section 4: Summary
In summary, the error "Permission denied (publickey) fatal - Could not read from remote repository" can occur when the user does not have the correct permissions to access the remote repository. To resolve this error, the user should check that their SSH key is in the correct format and associated with their account, that they have the correct permissions to access the remote repository, and that their connection is not being blocked by a firewall.
