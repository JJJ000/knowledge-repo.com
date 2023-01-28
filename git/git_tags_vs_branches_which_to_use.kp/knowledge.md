---
title: What is the distinction between a tag and a branch in git? which should I apply in this situation?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: A tag is used to mark a specific point in a repository`s history, while a branch is used to create a separate line of development. You should use a branch here.
---

**Contents**

[TOC]

#What is a Tag?
A tag is a reference to a specific point in a repository's history. It is usually used to mark a release or version of software. Tags are immutable and generally created to mark a specific point in time.

#What is a Branch?
A branch is a parallel version of a repository. It is contained within the repository, but does not affect the primary or master branch allowing you to work freely without disrupting the "live" version. When a certain point in the development cycle is reached, the changes can be merged back into the master branch.

#Which Should I Use?
The decision on which to use depends on the specific needs of the project. If you are looking to mark a specific point in the project's history, such as a release or version, then a tag is the right choice. If you are looking to work on a separate version of the project, such as a feature or bug fix, then a branch is the right choice.
