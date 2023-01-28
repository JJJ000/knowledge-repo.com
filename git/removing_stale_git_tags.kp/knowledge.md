---
title: Delete any git tags that are not present in the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git fetch --prune` to remove local git tags that are no longer on the remote repository.
---

**Contents**

[TOC]

1. List Local Git Tags
----------------------------------
To list the local git tags, use the following command:

```
git tag
```

2. Delete Local Git Tags
----------------------------------
To delete a local git tag, use the following command:

```
git tag -d <tag_name>
```

3. Fetch Remote Tags
----------------------------------
To fetch the remote tags, use the following command:

```
git fetch --tags
```

4. Delete Remote Tags
----------------------------------
To delete a remote tag, use the following command:

```
git push --delete origin <tag_name>
```
