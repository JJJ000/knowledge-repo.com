---
title: What steps are needed to configure a git project to use an external repository submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Clone the external repo as a submodule into the main project`s repository using the `git submodule add` command.
---

**Contents**

[TOC]

# Section 1: Initial Setup
1. Create a new git repository for your project.
2. Create a new folder in your repository to hold the external repo submodule.
3. Add the external repo as a submodule in the new folder.

# Section 2: Configuring the Submodule
1. Initialize the submodule with `git submodule init`.
2. Update the submodule with `git submodule update`.
3. Configure the submodule to track the external repo with `git config --file .gitmodules submodule.<submodule_name>.url <url_of_external_repo>`.

# Section 3: Committing Changes
1. Commit the changes to the submodule with `git commit -m "Added submodule <submodule_name> from <url_of_external_repo>".
2. Push the changes to the remote repository with `git push origin master`.

# Section 4: Updating the Submodule
1. Update the submodule with `git submodule update --remote`.
2. Commit the changes to the submodule with `git commit -m "Updated submodule <submodule_name>".
3. Push the changes to the remote repository with `git push origin master`.
