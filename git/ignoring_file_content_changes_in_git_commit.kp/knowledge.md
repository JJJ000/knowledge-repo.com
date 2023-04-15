---
title: Is it possible to commit a file and ignore any changes made to its contents?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can use the `--only` flag with `git commit` to commit a file without its content changes.
---

**Contents**

[TOC]

### Yes

It is possible to `git commit` a file and ignore its content changes. This can be done by using the `--allow-empty` flag when running the `git commit` command. This flag allows you to commit a file without its content changes being tracked. 

### How To

To `git commit` a file and ignore its content changes, use the following command:

```git
git commit --allow-empty <file_name>
```

This will create a commit for the specified file, but will not track any of its content changes.

### Benefits

Using the `--allow-empty` flag when running `git commit` allows you to commit files without tracking their content changes. This can be useful when you want to commit a file to a repository but don't want to track its content changes.

### Caveats

It is important to note that using the `--allow-empty` flag when running `git commit` will not track any of the file's content changes. If you want to track the content changes, you will need to commit the file without the `--allow-empty` flag.
