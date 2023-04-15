---
title: Remove all tags from a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To delete all tags from a Git repository, run the command `git tag -d <tag\_name>`.
---

**Contents**

[TOC]

### Deleting Tags Locally
1. Delete the tag from the local repository:
`git tag -d <tag_name>`

2. Push the changes to the remote repository:
`git push origin :refs/tags/<tag_name>`

### Deleting Tags Remotely
1. Delete the tag from the remote repository:
`git push --delete origin <tag_name>`

2. Remove the tag from the local repository:
`git tag -d <tag_name>`
