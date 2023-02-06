---
title: Deploy a non-master git branch to heroku
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can deploy a non-master branch to Heroku using the `--branch` flag.
---

**Contents**

[TOC]

# Section 1: Overview
Heroku is a cloud platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud. It supports a variety of programming languages, including Node.js, Python, Java, and PHP. Heroku allows developers to deploy applications from any non-master Git branch, making it easy to test and deploy changes quickly.

# Section 2: Benefits
Deploying from a non-master branch on Heroku has several benefits. For one, it allows developers to test changes in a non-production environment before pushing them to production. This eliminates the risk of introducing bugs into production and ensures that only tested and working code is deployed. Additionally, it allows developers to easily roll back changes if something goes wrong.

# Section 3: Steps
To deploy a non-master Git branch on Heroku, developers must first create a new branch from the master branch. This can be done using the git checkout command. Once the branch is created, developers can make any changes they need to the code and commit them to the branch. Finally, developers can deploy the branch to Heroku using the git push command.

# Section 4: Conclusion
Deploying from a non-master Git branch on Heroku is a great way to test changes in a non-production environment before pushing them to production. It also allows developers to easily roll back changes if something goes wrong. To deploy a non-master branch, developers must first create a new branch, make any necessary changes, and then push the branch to Heroku.
