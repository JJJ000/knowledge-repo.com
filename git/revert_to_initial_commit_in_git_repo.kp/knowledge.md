---
title: Reset the git repository to only contain the current commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Create a new repository and add the current commit to it using `git init; git add .; git commit -m <message>`.
---

**Contents**

[TOC]

### Create an Empty Repository

The first step is to create an empty repository on a Git hosting platform such as GitHub. This repository will be the destination for the current commit.

### Checkout the Current Commit

Next, the current commit needs to be checked out from the existing repository. This can be done using the `git checkout` command.

### Push the Current Commit

Once the current commit has been checked out, it can be pushed to the new repository. This can be done using the `git push` command.

### Reset the Repository

Finally, the repository needs to be reset in order to make the current commit the only commit. This can be done using the `git reset --hard` command. This will reset the repository to the current commit, making it the only commit in the repository.
