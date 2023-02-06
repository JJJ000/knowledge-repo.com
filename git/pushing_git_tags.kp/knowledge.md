---
title: Do tags created in git get pushed to remote repositories?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, git tags are pushed to remote repositories along with the commits they reference.
---

**Contents**

[TOC]

## Yes
Git tags are pushed to the remote repository along with the rest of the code. This allows other developers to access the same version of the code that was tagged.

## How to Push
To push a tag, use the `git push` command followed by the name of the tag. For example, to push a tag named "v1.0.0", the command would look like this: `git push v1.0.0`.

## Benefits
Pushing tags to the remote repository provides several benefits. It allows other developers to easily access the same version of the code that was tagged, and it allows for easy rollbacks if needed.

## Conclusion
In conclusion, git tags do get pushed as well. Pushing tags to the remote repository provides several benefits, including easy access to the same version of the code and the ability to easily rollback if needed.
