---
title: What is the process for removing a tag from a remote repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To delete a remote tag in Git, use the command `git push --delete <remote\_name> <tag\_name>`.
---

**Contents**

[TOC]

### Using the Command Line
1. Move to the local repository: `cd <repo_name>`
2. Fetch the tags from the remote repository: `git fetch --tags`
3. Delete the tag from the remote repository: `git push --delete origin <tag_name>`

### Using the GitHub UI
1. Navigate to the repository on GitHub.
2. Click on the "Releases" tab.
3. Click on the tag you want to delete.
4. Click the "Delete" button.
5. Confirm the deletion.
