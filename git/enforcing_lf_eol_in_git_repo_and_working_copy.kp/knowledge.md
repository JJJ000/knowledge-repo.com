---
title: Ensure that the line endings in the git repository and its working copy are set to lf (unix-style)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git can be configured to enforce LF eol in the repo and working copy by setting the core.eol configuration option.
---

**Contents**

[TOC]

#Section 1: Force LF eol in git repo

In order to force LF eol in the git repo, you need to configure the autocrlf setting for the repo. This setting can be configured globally or per repository.

To configure the autocrlf setting globally, run the following command:

```
git config --global core.autocrlf true
```

To configure the autocrlf setting per repository, run the following command from the root of the repository:

```
git config core.autocrlf true
```

#Section 2: Force LF eol in working copy

In order to force LF eol in the working copy, you need to configure the eol setting for the repo. This setting can be configured globally or per repository.

To configure the eol setting globally, run the following command:

```
git config --global core.eol lf
```

To configure the eol setting per repository, run the following command from the root of the repository:

```
git config core.eol lf
```
