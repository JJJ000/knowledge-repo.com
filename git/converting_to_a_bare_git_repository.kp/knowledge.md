---
title: What is the process for changing a regular git repository into a bare one?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run the command `git clone --bare <original-repo-url> <new-bare-repo-url>`.
---

**Contents**

[TOC]

### Back Up Existing Repository

Before converting a repository to a bare repository, it is important to back up the existing repository. This can be done by cloning the existing repository to a new directory.

### Convert to a Bare Repository

Once the existing repository has been backed up, the repository can be converted to a bare repository. This can be done by running the command `git clone --bare <existing-repository-url> <new-bare-repository-url>` in the terminal.

### Push to New Bare Repository

Once the new bare repository has been created, the existing repository can be pushed to the new bare repository. This can be done by running the command `git push --mirror <new-bare-repository-url>` in the terminal.

### Clean Up

Once the new bare repository has been successfully pushed to, the existing repository can be removed. This can be done by deleting the existing repository from the local machine.
