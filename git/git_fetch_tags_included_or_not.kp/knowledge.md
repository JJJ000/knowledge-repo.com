---
title: Would running "git fetch --tags" also include the results of running "git fetch"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, `git fetch --tags` includes `git fetch` as the `--tags` option simply adds the tags from the remote repository to the local repository.
---

**Contents**

[TOC]

Yes

### What Does "git fetch --tags" Do?

"git fetch --tags" is a command used to fetch all tags from a remote repository and download them to the local repository. This command allows you to keep your local repository up to date with the remote repository, including any tags that have been added.

### What Does "git fetch" Do?

"git fetch" is a command used to download objects and references from a remote repository. This command allows you to keep your local repository up to date with the remote repository, including any changes that have been made.

### Does "git fetch --tags" Include "git fetch"?

Yes, "git fetch --tags" includes "git fetch". "git fetch --tags" is essentially a combination of the two commands, allowing you to download both objects and references, as well as tags, from the remote repository.
