---
title: What is the command to show all tags and their associated messages in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can list all tags along with the full message in git by using the command `git tag -n`.
---

**Contents**

[TOC]

### Section 1 - List All Tags

To list all tags in a Git repository, use the command:

`git tag`

This will list all tags in the current repository.

### Section 2 - Show Tag Details

To show more details about a particular tag, use the command:

`git show <tagname>`

This will show the full message associated with the tag, along with other details such as the author, date, and commit hash.

### Section 3 - List All Tags With Messages

To list all tags along with their full messages, use the command:

`git for-each-ref --format="%(refname:short) %(subject)" refs/tags`

This will list all tags along with the full message associated with each tag.

### Section 4 - List All Tags With Messages and Commit Hash

To list all tags along with their full messages and commit hash, use the command:

`git for-each-ref --format="%(refname:short) %(subject) %(objectname)" refs/tags`

This will list all tags along with the full message associated with each tag and the commit hash.
