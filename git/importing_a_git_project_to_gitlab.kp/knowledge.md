---
title: How can I bring an existing git project into gitlab?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Clone the existing project from its git repository into GitLab.
---

**Contents**

[TOC]

# Section 1: Clone the Project

The first step is to clone the existing project from its remote repository (e.g. GitHub) into your local machine. This can be done by running the following command:

`git clone <repository-url>`

Where `<repository-url>` is the URL of the remote repository.

# Section 2: Create a New Project in GitLab

Next, create a new project in GitLab. This can be done by navigating to the projects page in GitLab and clicking the "New Project" button.

# Section 3: Push the Project to GitLab

Once the project has been created, push the existing project to the new GitLab project. This can be done by running the following commands:

`git remote add gitlab <gitlab-repository-url>`

`git push -u gitlab master`

Where `<gitlab-repository-url>` is the URL of the newly created GitLab project.

# Section 4: Verify the Project is in GitLab

Finally, verify that the project has been successfully pushed to GitLab. This can be done by navigating to the project in GitLab and confirming that the files and commits from the existing project are present.
