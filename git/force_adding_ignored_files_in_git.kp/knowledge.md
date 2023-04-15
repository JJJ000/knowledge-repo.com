---
title: Add the file despite the exclusion specified in the .gitignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can force add a file to the repository despite the .gitignore file.
---

**Contents**

[TOC]

### Yes

1. Use the `--force` option when adding the file:

```git
git add --force <filename>
```

2. Use the `-f` option when adding the file:

```git
git add -f <filename>
```

### No

1. Edit the .gitignore file to stop ignoring the file you want to add.

2. Remove the file from the .gitignore file and commit the change.

3. Add the file to the repository.
