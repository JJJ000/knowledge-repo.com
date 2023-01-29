---
title: What is the process for duplicating a job in jenkins?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can clone a Jenkins job in Git by using the `Clone Job` option in the Jenkins UI.
---

**Contents**

[TOC]

### Cloning a Job in Jenkins

### Prerequisites 
Before cloning a job in Jenkins, it is important to have the following prerequisites: 
- A Jenkins instance with a job already configured 
- Git installed and configured on the Jenkins instance 

### Cloning the Job 
1. Navigate to the job you wish to clone in the Jenkins dashboard.
2. Click the "Configure" option in the left sidebar.
3. Scroll to the bottom of the page and click the "Git" button.
4. Enter the URL of the git repository you wish to clone the job from.
5. Click the "Save" button at the bottom of the page.

### Testing the Cloned Job 
Once the job has been cloned, it is important to test it to make sure it is working correctly. To do this: 
1. Navigate to the cloned job in the Jenkins dashboard.
2. Click the "Build Now" button in the left sidebar.
3. Monitor the progress of the build in the "Build History" section.
4. Once the build is complete, check the console output to ensure that the job was successful.
