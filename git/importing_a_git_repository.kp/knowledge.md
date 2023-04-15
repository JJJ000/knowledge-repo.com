---
title: What is the process for transferring an existing git repository to another?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run the command `git remote add <new\_remote\_name> <repository\_url>` to import an existing Git repository into another.
---

**Contents**

[TOC]

### 1. Clone the Repository

The first step is to clone the existing repository into a new directory. This can be done by running the following command:

`git clone <source_repo_url> <destination_directory>`

### 2. Add a New Remote

Once the repository is cloned, add a new remote to the cloned repository. This can be done using the following command:

`git remote add <new_remote_name> <new_repo_url>`

### 3. Push to the New Remote

The next step is to push the existing repository to the new remote. This can be done using the following command:

`git push -u <new_remote_name> master`

### 4. Verify the Push

Finally, verify that the push was successful by running the following command:

`git remote -v`

This will show the new remote and its URL.
