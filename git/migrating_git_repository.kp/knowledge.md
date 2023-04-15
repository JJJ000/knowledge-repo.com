---
title: What is the process for transferring a git repository from one server to another?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The recommended way to migrate a Git repository from one server to a new one is to use the git clone command to clone the repository from the old server to the new one.
---

**Contents**

[TOC]

### Preparing to Migrate

1. Backup the existing repository on the old server by cloning it onto a local machine.

2. Create a new repository on the new server.

### Transferring the Repository

1. Push the cloned repository from the local machine to the new repository on the new server.

2. Verify the contents of the new repository on the new server.

### Updating Remote URLs

1. Change the remote URLs of the local repository to point to the new repository on the new server.

2. Push the changes to the new repository on the new server.

### Verifying the Migration

1. Pull the latest changes from the new repository on the new server to the local machine.

2. Verify that all the changes were migrated successfully.
