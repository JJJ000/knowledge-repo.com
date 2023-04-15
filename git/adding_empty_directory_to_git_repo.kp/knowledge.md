---
title: What is the process for adding an empty directory to a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Create an empty file named `.gitkeep` in the directory and add it to the repository.
---

**Contents**

[TOC]

### 1. Create the Directory

Create the directory you want to add to the Git repository. This can be done using the command line or by using a file explorer.

### 2. Add Directory to Repository

Once the directory has been created, you can add it to the Git repository by using the `git add` command. For example, if the directory is named "mydir", you can add it to the repository with the command `git add mydir`.

### 3. Commit Changes

After the directory has been added to the repository, you need to commit the changes so that they are recorded in the repository. This can be done with the `git commit` command. For example, to commit the changes with the message "Added mydir directory", you can use the command `git commit -m "Added mydir directory"`.

### 4. Push to Remote

Finally, you need to push the changes to the remote repository so that they are available to other users. This can be done with the `git push` command. For example, to push the changes to the remote repository, you can use the command `git push origin master`.
