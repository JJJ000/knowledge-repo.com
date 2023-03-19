---
title: How to use Python unit tests in jenkins?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Python unittests can be integrated into Jenkins by using the Jenkins plugins such as the Jenkins PyUnit plugin, Jenkins xUnit plugin and Jenkins Cucumber reports plugin.
---

**Contents**

[TOC]

# Introduction

Jenkins is an open-source automation server that allows you to automate various aspects of software development. One of the things Jenkins can do is run unit tests for your Python code. Unit tests are automated tests that verify individual units of source code. In this article, we will discuss how to run Python unittests in Jenkins.

# Setting Up the Environment

Before we start setting up Jenkins to run Python unittests, we need to make sure that our development environment is set up correctly. Here are the steps:

1. Make sure that Python is installed on your system
2. Install the `unittest` module if it's not already installed
3. Write your Python unittests

# Configuring Jenkins to Run Python Unittests

Now that our development environment is set up, we can configure Jenkins:

1. Install the Jenkins server on your system
2. Install the `Jenkins Python plugin`
3. Create a new Jenkins job
4. Configure the job to execute your Python unittests

# Running Python Unittests in Jenkins

To run Python unittests in Jenkins, you need to tell Jenkins how to execute your tests. Here's how you can do it:

1. Go to the configuration page of the Jenkins job you created
2. Under the "Build" section, click "Add build step"
3. Choose "Execute shell"
4. In the command box, type the command to run your Python unittests
5. Save the configuration

Now, whenever you run the Jenkins job, your Python unittests will be executed and the results will be displayed in the Jenkins console output.
