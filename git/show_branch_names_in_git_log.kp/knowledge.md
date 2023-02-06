---
title: What command can I use to display the branch names in the "git log" output?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Include the `--decorate` flag when running `git log` to show the name of branches.
---

**Contents**

[TOC]

1. Configure the Log Format 

Git provides a powerful way to customize the log format to show the branch name. To do this, you can use the `--pretty` option and specify a custom format. For example, you can use the following command to show the branch name in the log:

```
git log --pretty=format:"%h %d %s (%cr) [%an]"
```

2. Include the `%d` Placeholder

The `%d` placeholder is used to show the ref names of the commits. You can use it to show the branch name. For example, the following command will show the branch name in the log:

```
git log --pretty=format:"%h %d %s (%cr) [%an]" --decorate
```

3. Use the `--decorate` Option

The `--decorate` option is used to show the ref names of the commits. It is used in combination with the `%d` placeholder to show the branch name in the log. For example, the following command will show the branch name in the log:

```
git log --pretty=format:"%h %d %s (%cr) [%an]" --decorate
```

4. Use the `--graph` Option

The `--graph` option is used to show the commit graph in the log. It is used in combination with the `--decorate` option and the `%d` placeholder to show the branch name in the log. For example, the following command will show the branch name in the log:

```
git log --graph --pretty=format:"%h %d %s (%cr) [%an]" --decorate
```
