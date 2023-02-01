---
title: Specify a direct github source in requirements.txt
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In requirements.txt, specify the github source with the format `git+<git-repo-url>@<commit-ish>#egg=<package-name>`.
---

**Contents**

[TOC]

# Section 1: Format
The format for a direct GitHub source in Python is as follows:

`git+git://github.com/[user]/[repo].git@[branch]`

# Section 2: User
The [user] part of the format is the username of the GitHub user who owns the repository.

# Section 3: Repository
The [repo] part of the format is the name of the repository to be sourced from.

# Section 4: Branch
The [branch] part of the format is the name of the branch of the repository to be sourced from.
