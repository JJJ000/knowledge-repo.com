---
title: Fetch a particular commit from a remote git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To retrieve a specific commit from a remote Git repository, use the `git fetch` command followed by the commit`s SHA-1 hash.
---

**Contents**

[TOC]

# Retrieve a Specific Commit

## Step 1: Find the Specific Commit

The first step in retrieving a specific commit from a remote Git repository is to find the commit you are looking for. This can be done by using the `git log` command to view all of the commits in the repository. You can filter the commits by author, date, and message.

## Step 2: Check Out the Specific Commit

Once you have identified the specific commit you are looking for, you can check it out from the remote repository. To do this, you can use the `git checkout` command followed by the commit hash. This will create a local copy of the commit on your machine.

## Step 3: Push the Commit to a Remote Repository

The final step is to push the commit to a remote repository. You can do this by using the `git push` command followed by the remote repository URL and the commit hash. This will push the commit to the remote repository and make it available for anyone to access.

## Step 4: Verify the Commit

Once the commit has been pushed to the remote repository, you can verify that it was successful by using the `git log` command to view the commit history. This will show the commit that you just pushed and allow you to verify that it was successful.
