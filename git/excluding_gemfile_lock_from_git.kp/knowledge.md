---
title: Should the gemfile.lock file be excluded from version control by including it in the .gitignore file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, Gemfile.lock should be included in .gitignore.
---

**Contents**

[TOC]

####Yes

Gemfile.lock should be included in .gitignore because it is an automatically generated file that is not necessary to track in the repository. This file should not be committed to the repository as it will cause conflicts when other developers attempt to run bundle install.

####No

Gemfile.lock should not be included in .gitignore because it is an important file that contains the exact versions of gems that are installed in the application. This is necessary for developers to have a consistent environment when running the application.
