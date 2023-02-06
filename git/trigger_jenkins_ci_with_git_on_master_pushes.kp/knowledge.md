---
title: What steps do I need to take to configure jenkins ci and git to trigger on pushes to the master branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Enable the `Build when a change is pushed to GitHub` option in the Jenkins job configuration.
---

**Contents**

[TOC]

1. Setting Up Jenkins 
    * Install Jenkins on your server and configure the necessary plugins. 
    * Create a new job on Jenkins and configure it to pull from your Git repository. 
    * Under Source Code Management, select Git and enter the URL of your repository. 

2. Setting Up Git 
    * Create a webhook in your Git repository to trigger a Jenkins build when code is pushed to the master branch. 
    * Under the repository settings, select Webhooks and add a new webhook. 
    * Enter the URL of your Jenkins server, select the Push event, and save the webhook.

3. Configuring Jenkins 
    * In the Jenkins job configuration, select the "Build when a change is pushed to Git" option. 
    * Select the master branch and save the changes. 

4. Testing 
    * Push a change to the master branch and check if the Jenkins build is triggered. 
    * If the build is triggered, the Jenkins job is now configured to build when a change is pushed to the master branch.
