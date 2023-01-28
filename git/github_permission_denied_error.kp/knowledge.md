---
title: You do not have the necessary authorization to access this github page (public key authentication failed)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: This error message indicates that the user does not have the correct public key associated with their account.
---

**Contents**

[TOC]

### Overview

This error message is thrown when a user attempts to access a repository on GitHub, but the user does not have the correct authentication credentials. This usually occurs when the user is trying to access a private repository and does not have the appropriate SSH key configured on their account. 

### Causes

The most common cause of this error message is that the user does not have the correct SSH key configured on their GitHub account. This key is used to authenticate the user and allow them to access the repository. 

Another possible cause is that the user does not have the correct permissions to access the repository. This could be due to the repository being private and the user not having been added to the list of collaborators. 

### Solution

To resolve this issue, the user should ensure that their SSH key is correctly configured on their GitHub account. If they do not have an SSH key, they should generate one and add it to their account. 

The user should also ensure that they have been added to the list of collaborators for the repository if it is private. The repository owner should be able to add the user to the list of collaborators.
