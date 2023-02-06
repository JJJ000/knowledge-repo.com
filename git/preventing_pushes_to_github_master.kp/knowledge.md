---
title: How can we avoid pushing to the master branch on github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a branch policy requiring all changes to be approved before merging into the master branch.
---

**Contents**

[TOC]

# Preventing Pushes to Master on GitHub

## 1. Create a Separate Branch

The most straightforward way to prevent pushing to master on GitHub is to create a separate branch for all development work. This branch should be used for all code changes, bug fixes, and feature additions. The master branch should only be used for releases and should not be used for development work.

## 2. Set Up a Branch Protection Rule

GitHub allows users to set up branch protection rules that prevent pushes to the master branch. This rule can be configured to require pull requests and code reviews before any code is merged into the master branch. This ensures that all code changes are reviewed before they are merged, and prevents any pushes to the master branch without review.

## 3. Use a Continuous Integration Tool

Continuous integration tools such as Jenkins or Travis CI can be used to automate the process of building and testing code. This ensures that all code changes are tested before they are merged into the master branch, and prevents any code changes that are not passing tests from being merged.

## 4. Use a Git Hook

Git hooks can be used to prevent pushes to the master branch. This can be done by creating a pre-push hook that prevents any pushes to the master branch. This ensures that all code changes are reviewed before they are pushed, and prevents any pushes to the master branch without review.
