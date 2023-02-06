---
title: Have git automatically strip trailing white space before committing
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git can be configured to automatically remove trailing white space before committing by setting the `whitespace` option in the .gitattributes file.
---

**Contents**

[TOC]

## Option 1

You can configure Git to automatically remove trailing whitespace before committing by adding the following line to your `.gitconfig` file: 

```
[core]
    whitespace = fix,-indent-with-non-tab,trailing-space
```

## Option 2

You can also set up a pre-commit hook to strip out trailing whitespace before committing. To do this, create a file named `pre-commit` in the `.git/hooks` directory and add the following code to the file:

```
#!/bin/sh
git diff --staged --check | grep -E '^(+|-)[^+-]' | grep -E '[ \t]+$' | cut -c-40 | sort | uniq | while read line; do
    sed -i '' -e "s/$line/`echo $line | sed 's/[ \t]*$//'`/" "$line"
done
```

## Option 3

You can also use a Git filter to automatically remove trailing whitespace before committing. To do this, add the following line to your `.gitconfig` file:

```
[filter "whitespace"]
    clean = "sed 's/[ \t]*$//'"
```

## Option 4

You can also use a third-party tool such as `pre-commit` to automatically remove trailing whitespace before committing. To do this, install the `pre-commit` tool and add the following line to your `.pre-commit-config.yaml` file:

```
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.4.0
    hooks:
    -   id: trailing-whitespace
```
