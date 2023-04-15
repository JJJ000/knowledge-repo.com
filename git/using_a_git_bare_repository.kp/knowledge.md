---
title: What is the purpose of using the "git --bare init" repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git --bare init is used to create a new, empty, bare repository in the current directory.
---

**Contents**

[TOC]

### Setting up a Bare Repository

1. Create a directory for the repository: 
    `mkdir my_repo`

2. Change the directory to the newly created repository: 
    `cd my_repo`

3. Initialize the repository using the `git --bare init` command:
    `git --bare init`

### Cloning the Bare Repository

1. Change the directory to the location where the new working copy should be created: 
    `cd ~/my_projects`

2. Clone the repository using the `git clone` command: 
    `git clone ~/my_repo`

3. Change the directory to the newly cloned repository: 
    `cd my_repo`
