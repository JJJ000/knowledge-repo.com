---
title: Replace the local file with the version in the remote repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can force overwrite of local file with what`s in origin repo by using the `git fetch --all` and `git reset --hard origin/master` commands.
---

**Contents**

[TOC]

### git fetch

The `git fetch` command can be used to overwrite a local file with what is in the origin repository. This command downloads all the changes from the remote repository, but does not merge them with the local repository.

### git reset

Once the changes have been downloaded, the `git reset` command can be used to overwrite the local file with the version from the origin repository. This command resets the local repository to the state of the origin repository.

### git checkout

The `git checkout` command can also be used to overwrite a local file with the version from the origin repository. This command will check out the file from the origin repository and overwrite the local file.

### git pull

Finally, the `git pull` command can be used to both download the changes from the origin repository and merge them with the local repository. This command will overwrite the local file with the version from the origin repository.
