---
title: Look through the entire git repository for a particular string
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the command `git log -S <string>` to search all of Git history for a given string.
---

**Contents**

[TOC]

1. Prerequisites
--------------------
Before you can search your Git history for a string, you'll need to have a Git repository set up and have committed some changes.

2. Using Git Log
--------------------
The simplest way to search your Git history for a string is to use the `git log` command. This command will show the commit history of your repository, and you can use the `--grep` option to search for a specific string.

For example, if you wanted to search for the string "foo", you would run the following command:

```git
git log --grep="foo"
```

This will search the commit messages for any commits that contain the string "foo".

3. Using Git Grep
--------------------
Another way to search your Git history for a string is to use the `git grep` command. This command will search the contents of all of your files for a specific string.

For example, if you wanted to search for the string "foo", you would run the following command:

```git
git grep "foo"
```

This will search all of the files in your repository for any occurrences of the string "foo".

4. Using a GUI
--------------------
If you'd prefer to use a graphical user interface (GUI) to search your Git history for a string, there are a number of options available. For example, many popular Git clients such as GitHub Desktop and GitKraken offer a built-in search feature that allows you to search your repository's history for a string.
