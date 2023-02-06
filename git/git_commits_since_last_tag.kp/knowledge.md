---
title: Retrieve all git commits since the most recent tag
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git log $(git describe --tags --abbrev=0)..HEAD` to get all git commits since the last tag.
---

**Contents**

[TOC]

1. Creating a Tag
To get all the git commits since the last tag, the first step is to create a tag. To do this, use the `git tag` command.

2. Finding the Last Tag
The next step is to find the last tag that was created. This can be done by using the `git tag -l` command, which will list all the tags that have been created.

3. Getting the Commits
Once the last tag has been identified, the next step is to get all the commits since that tag. This can be done by using the `git log` command with the `--since` option, followed by the tag name.

4. Viewing the Commits
The final step is to view the commits that have been retrieved. This can be done by using the `git show` command with the commit hash. This will show the commit details, including the files that were changed, the author, and the commit message.
