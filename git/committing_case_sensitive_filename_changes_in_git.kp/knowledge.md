---
title: What is the best way to make sure git only recognizes changes in filenames that are case-sensitive?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `-i` option when committing to make Git ignore case-sensitive filename changes.
---

**Contents**

[TOC]

### Add Files

In order to commit case-sensitive only filename changes in Git, the first step is to add the files to the repository. This can be done by running the `git add` command with the name of the file. For example, if you wanted to add a file called `File.txt`, you would run `git add File.txt`.

### Check Status

After adding the files, it is important to check the status of the repository. This can be done by running the `git status` command. This will show a list of all the files that have been added and any other changes that have been made to the repository.

### Commit Changes

Once the status of the repository has been checked, the changes can then be committed. This is done by running the `git commit` command with a message describing the changes that have been made. For example, if you were committing case-sensitive only filename changes, you could use the message "Committing case-sensitive only filename changes".

### Push Changes

Finally, the changes need to be pushed to the remote repository. This is done by running the `git push` command. This will push the changes to the remote repository and make them available to other users.
