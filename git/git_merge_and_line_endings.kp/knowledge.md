---
title: Can git-merge overlook line-ending disparities?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, git-merge cannot ignore line-ending differences.
---

**Contents**

[TOC]

## Yes

Git merge can ignore line-ending differences by setting the `core.autocrlf` configuration parameter to `false`. This will disable the automatic conversion of line endings to the system's native format.

## How to Set `core.autocrlf`

The `core.autocrlf` parameter can be set in the `.gitconfig` file. To do this, open the file in a text editor and add the following line:

`[core]`
`autocrlf = false`

## Benefits

Setting `core.autocrlf` to `false` will ensure that line endings are not automatically converted. This will help to prevent conflicts during merges caused by differences in line endings.

## Disadvantages

The main disadvantage of setting `core.autocrlf` to `false` is that it may cause issues when working with files that require specific line endings. For example, Windows-based text files may not be readable on other operating systems if the line endings are not converted to the system's native format.
