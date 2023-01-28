---
title: Push specific lines of a file to a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git add -p` command to selectively commit specific lines of a file to git.
---

**Contents**

[TOC]

### Step 1: Staging the File

Before committing specific lines of a file to git, the file must first be staged. This is done by running the command `git add <file-name>`, where `<file-name>` is the name of the file to be committed.

### Step 2: Selecting the Lines

Next, the specific lines of the file to be committed must be selected. This can be done using the command `git checkout -p <file-name>`, where `<file-name>` is the name of the file to be committed. This will bring up a prompt that will allow the user to select the specific lines to be committed.

### Step 3: Committing the Lines

Once the lines have been selected, they can be committed with the command `git commit -m "<message>"`, where `<message>` is a description of the commit.

### Step 4: Pushing the Commit

Finally, the commit can be pushed to the remote repository with the command `git push`. This will ensure that the changes are pushed to the remote repository and are available for other users to view.
