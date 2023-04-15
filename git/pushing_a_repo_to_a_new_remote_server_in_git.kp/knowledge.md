---
title: Push an existing repository from its current remote server to a new and different remote repository server
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git remote add <new\_remote\_name> <new\_remote\_url>`, followed by `git push -u <new\_remote\_name> master` to push an existing repo to a new and different remote repo server.
---

**Contents**

[TOC]

### Step 1: Create a New Remote Repository

Create a new repository on your remote server, following the instructions provided by the server.

### Step 2: Add the New Remote Repository to Your Local Repository

Run the following command to add the new remote repository to your local repository:

```git
git remote add <new-remote-name> <url-of-new-remote-repo>
```

### Step 3: Push Your Local Repository to the New Remote Repository

Run the following command to push your local repository to the new remote repository:

```git
git push <new-remote-name> <branch-name>
```

### Step 4: Verify the Push

Run the following command to verify that your local repository was successfully pushed to the new remote repository:

```git
git remote -v
```

The output should show the new remote repository URL listed alongside your local repository URL.
