---
title: What is the process for updating the address of a remote git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To change the URI for a remote Git repository, use the `git remote set-url` command.
---

**Contents**

[TOC]

### Checking the Current URI

To check the current URI for a remote Git repository, use the `git remote show` command. This will list all the remote repositories associated with the local repository, including the name and URI of each.

### Updating the URI

To update the URI for a remote Git repository, use the `git remote set-url` command. This command takes two arguments: the name of the remote repository, and the new URI. For example, to change the URI for a remote named `origin` to `https://example.com/myrepo.git`, the command would be:

```shell
git remote set-url origin https://example.com/myrepo.git
```

### Verifying the Change

Once the URI has been updated, it's a good idea to verify that the change has been successful. To do this, use the `git remote show` command again. This will list all the remote repositories associated with the local repository, including the name and URI of each. The new URI should now be visible.

### Pushing to the New URI

Finally, to push any changes to the new URI, use the `git push` command. This will push all changes to the remote repository, using the new URI.
