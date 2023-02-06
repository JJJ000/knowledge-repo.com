---
title: Display creation dates of all lightweight tags using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The command `git for-each-ref --sort=-taggerdate --format `%(refname) %(taggerdate)` refs/tags` can be used to show all lightweight tags creation dates.
---

**Contents**

[TOC]

#1 Git Tag Command
`git tag`

#2 List All Tags
`git tag -l`

#3 List All Tags with Dates
`git log --tags --simplify-by-decoration --pretty="format:%ai %d"`

#4 List All Lightweight Tags with Dates
`git log --tags=<tag-name> --simplify-by-decoration --pretty="format:%ai %d"`
