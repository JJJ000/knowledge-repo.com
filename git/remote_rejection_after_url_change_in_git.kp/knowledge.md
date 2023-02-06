---
title: The git remote url was changed, but the remote rejected the update because shallow updates are not allowed
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The remote rejected the update because shallow updates are not allowed.
---

**Contents**

[TOC]

# Overview

When attempting to change the Git remote URL, the remote may reject the update if a shallow update is not allowed. This article will explain what a shallow update is and how to resolve the issue when the remote rejects the update.

# What is a Shallow Update?

A shallow update is a type of update that only pulls down the most recent commit from the remote repository. This type of update is useful when you want to quickly pull down the latest changes without having to clone the entire repository. However, some remotes may not allow shallow updates and will reject any attempt to change the remote URL if a shallow update is attempted.

# How to Resolve

To resolve the issue of the remote rejecting the update, you will need to clone the entire repository and then push the changes to the new remote URL. This will ensure that all of the commits from the original repository are included in the new remote URL.

# Conclusion

When attempting to change the Git remote URL, the remote may reject the update if a shallow update is not allowed. To resolve this issue, you will need to clone the entire repository and then push the changes to the new remote URL. This will ensure that all of the commits from the original repository are included in the new remote URL.
