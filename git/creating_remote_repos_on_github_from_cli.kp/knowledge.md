---
title: Can you make a remote repository on github using the command line without accessing a web browser?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, it is possible to create a remote repo on GitHub from the CLI using the `git push` command.
---

**Contents**

[TOC]

### Yes

GitHub allows users to create a remote repository from the command line. This can be done by first logging in to GitHub from the command line, then running the `gh repo create` command.

### Steps

1. Log in to GitHub from the command line. This can be done by running the command `gh auth login`.

2. Create the remote repository. This can be done by running the command `gh repo create [repo name]`.

3. Push the local repository to the remote repository. This can be done by running the command `git push -u origin master`.

### Conclusion

By following these steps, users can create a remote repository on GitHub from the command line without needing to open a browser.
