---
title: What is the process for updating/upgrading a package using pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To update/upgrade a package using pip in Python, use the command `pip install --upgrade <package-name>`.
---

**Contents**

[TOC]

# Updating a Package Using Pip

## Step 1: Check for Package Updates
Before updating a package, it is important to check if there are any available updates. This can be done by running the command `pip list --outdated`. This will list all the packages that have updates available. 

## Step 2: Update the Package
Once you have identified the package you would like to update, you can update it by running the command `pip install --upgrade <package name>`. This will upgrade the package to the latest version. 

## Step 3: Confirm the Update
Once the package has been updated, you can confirm the update by running the command `pip list --outdated`. This will list all the packages that have updates available. The package you updated should no longer be listed. 

## Step 4: Verify the Update
You can verify the update by running the command `pip show <package name>`. This will show the version of the package that is currently installed. You can compare this to the version of the package available on the Python Package Index to ensure that the package has been successfully updated.
