---
title: Receiving error code 403 fatal when attempting to push to git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: This error indicates that the server is refusing access due to authentication issues.
---

**Contents**

[TOC]

### Overview

When attempting to push to a Git repository, a 403 error code indicates that the user does not have the necessary permissions to push to the repository. This error can occur for various reasons, including incorrect authentication credentials, incorrect repository permissions, or a server-side issue. 

### Causes

The most common cause of a 403 error when pushing to a Git repository is incorrect authentication credentials. If the user is attempting to push to a private repository, they must authenticate with their username and password or with a personal access token. If the user is attempting to push to a public repository, they must authenticate with their username and an SSH key. 

Incorrect repository permissions can also cause a 403 error when pushing to a Git repository. If the user does not have the necessary permissions to push to the repository, they will receive a 403 error. 

Finally, a server-side issue can also cause a 403 error when pushing to a Git repository. If the server is experiencing an issue, it may prevent the user from pushing to the repository. 

### Solutions

To resolve a 403 error when pushing to a Git repository, the user should first check their authentication credentials. If they are attempting to push to a private repository, they should ensure that they are authenticating with their username and password or with a personal access token. If they are attempting to push to a public repository, they should ensure that they are authenticating with their username and an SSH key. 

The user should also check the repository permissions to ensure that they have the necessary permissions to push to the repository. If they do not have the necessary permissions, they should contact the repository owner to request access. 

Finally, the user should check to see if the server is experiencing an issue. If the server is experiencing an issue, they should contact the server administrator to resolve the issue.
