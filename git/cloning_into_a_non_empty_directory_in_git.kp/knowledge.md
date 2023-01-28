---
title: How can I clone a repository into a directory that already contains files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git clone <url> <directory>` with the existing directory as the <directory> argument.
---

**Contents**

[TOC]

### Cloning into a Non-Empty Directory

Git allows you to clone a repository into an existing, non-empty directory. This can be useful if you want to add a repository to an existing project.

### Prerequisites

Before cloning into a non-empty directory, you should make sure that the directory is empty or contains only files that are not tracked by Git. If the directory contains files that are tracked by Git, the clone will fail.

### Cloning the Repository

To clone a repository into a non-empty directory, use the `git clone` command with the `--no-checkout` option. This will clone the repository without checking out any of the files, allowing you to add them to the existing directory.

```
git clone <repository-url> --no-checkout
```

### Adding the Cloned Files to the Existing Directory

Once the repository has been cloned, you can use the `git add` command to add the cloned files to the existing directory.

```
git add <path-to-cloned-files>
```
