---
title: Do I need to include the django migration files in the .gitignore file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, the Django migration files should be added to the .gitignore file.
---

**Contents**

[TOC]

#### Yes

- Django migration files are generated automatically as part of the Django project and are not necessary to track in the version control system.
- Adding them to the .gitignore file will prevent them from being committed to the repository.

#### No

- Django migration files can be useful for tracking the changes that have been made to the database schema.
- If the project is being worked on by multiple developers, it can be helpful to commit the migration files to the repository so everyone is working with the same version of the database schema.
