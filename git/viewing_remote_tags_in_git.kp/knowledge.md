---
title: What is the procedure for viewing remote tags?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the command `git ls-remote --tags` to see remote tags in Git.
---

**Contents**

[TOC]

# Section 1: List Remote Tags

To list all remote tags in Git, use the command `git ls-remote --tags <remote>`. Replace `<remote>` with the remote repository URL.

# Section 2: View Remote Tag Details

To view the details of a specific remote tag, use the command `git show <tag>`. Replace `<tag>` with the name of the tag. This command will show the tag details, such as the tagger, date, message, and commit hash.

# Section 3: Fetch and Checkout Remote Tag

To fetch and checkout a remote tag, use the command `git fetch --tags <remote>`. Replace `<remote>` with the remote repository URL. This will fetch all remote tags from the repository. To checkout the tag, use the command `git checkout <tag>`. Replace `<tag>` with the name of the tag.

# Section 4: Push and Delete Remote Tag

To push a local tag to a remote repository, use the command `git push <remote> <tag>`. Replace `<remote>` with the remote repository URL and `<tag>` with the name of the tag. To delete a remote tag, use the command `git push <remote> :refs/tags/<tag>`. Replace `<remote>` with the remote repository URL and `<tag>` with the name of the tag.
