---
title: Are git tags only applicable to the current branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, Git tags can be applied to any commit in any branch.
---

**Contents**

[TOC]

# No

Git tags do not only apply to the current branch. They can be associated with any commit in the repository, regardless of the branch.

# How to Apply a Tag

A tag can be applied to any commit in the repository. To do this, use the `git tag` command followed by the tag name and the commit hash. For example, `git tag v1.0.0 4d2f6d`.

# How to View Tags

To view all tags in the repository, use the `git tag` command without any arguments. This will list all tags in the repository, along with their associated commit hashes.

# How to Push Tags

Once a tag is created, it must be pushed to the remote repository. To do this, use the `git push` command followed by the tag name. For example, `git push v1.0.0`. This will push the tag to the remote repository, where it can be viewed by other users.
