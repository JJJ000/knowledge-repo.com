---
title: What is the process for comparing two tags using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To compare two tags with git, use the command `git diff <tag1> <tag2>`.
---

**Contents**

[TOC]

#1 Comparing Tags Using Git Diff

1. Checkout the tag you want to compare: `git checkout <tag1>`
2. Compare the tag with another tag: `git diff <tag2>`

#2 Comparing Tags Using Git Log

1. Checkout the tag you want to compare: `git checkout <tag1>`
2. List the commits between the two tags: `git log <tag2>..<tag1>`

#3 Comparing Tags Using Git Tag

1. List all tags: `git tag`
2. Compare the tags: `git tag -v <tag1> <tag2>`

#4 Comparing Tags Using Git Show

1. Checkout the tag you want to compare: `git checkout <tag1>`
2. Show the differences between the two tags: `git show <tag2>`
