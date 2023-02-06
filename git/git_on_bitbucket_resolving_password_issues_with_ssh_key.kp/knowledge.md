---
title: I am constantly prompted for a password when using git on bitbucket, even though I have uploaded my public ssh key
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The SSH key may not be configured correctly in the Bitbucket settings.
---

**Contents**

[TOC]

# Overview
Git is a distributed version control system used for software development and other version control tasks. Bitbucket is a web-based hosting service for projects that use the Git version control system. It is often necessary to authenticate with Bitbucket using SSH keys in order to access a repository. However, even after uploading a public SSH key to Bitbucket, some users may still be prompted for a password when attempting to access a repository.

# Possible Causes
There are a few potential causes for this issue. First, it is possible that the public SSH key was not uploaded correctly. It is also possible that the SSH key is not registered in the correct user account. Additionally, if the SSH key is too long, it may not be accepted by Bitbucket.

# Troubleshooting
To troubleshoot this issue, the first step is to ensure that the SSH key was uploaded correctly. If the SSH key was uploaded correctly, then the next step is to check that the SSH key is registered in the correct user account. If the SSH key is too long, it may need to be shortened.

# Conclusion
In summary, if a user is prompted for a password even after uploading a public SSH key to Bitbucket, there are a few potential causes that may need to be addressed. These include ensuring the SSH key was uploaded correctly, checking that the SSH key is registered in the correct user account, and potentially shortening the SSH key.
