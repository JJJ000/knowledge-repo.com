---
title: Can different projects have separate git configurations?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, it is possible to have different Git configuration for different projects by using the `--local` flag when running Git commands.
---

**Contents**

[TOC]

### Yes

Git allows users to have different configurations for different projects. This is done by setting up different configurations for each project in the `.git/config` file.

### How

The `.git/config` file is where Git stores all of its configuration settings. To set up different configurations for each project, users can add a new section to the `.git/config` file for each project. Each section should have a unique name and contain the configuration settings for that project.

### Benefits

Having different configurations for each project can be useful for managing multiple projects with different requirements. For example, if one project requires different commit messages than another, the user can set up different configurations for each project to ensure that the correct commit messages are used.

### Examples

For example, the following `.git/config` file contains two different configurations for two different projects:

```
[project1]
    commitMsg = "Project 1 commit message"

[project2]
    commitMsg = "Project 2 commit message"
```
