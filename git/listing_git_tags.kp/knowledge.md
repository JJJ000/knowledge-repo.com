---
title: What is the command to view all git tags?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run the command `git tag` to list all Git tags.
---

**Contents**

[TOC]

### Using `git tag` Command

1. To list all tags in the local repository, use the following command:

```
git tag
```

2. To list all tags in the remote repository, use the following command:

```
git ls-remote --tags
```

### Using `git for-each-ref` Command

1. To list all tags in the local repository, use the following command:

```
git for-each-ref --sort=-taggerdate --format '%(refname:short)' refs/tags
```

2. To list all tags in the remote repository, use the following command:

```
git ls-remote --tags | awk -F / '{print $3}'
```
