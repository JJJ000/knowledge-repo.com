---
title: How does a tracking branch work?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A tracking branch in Git is a local branch that is connected to a remote branch, allowing the local branch to stay up to date with any changes to the remote branch.
---

**Contents**

[TOC]

## Definition

A tracking branch in Git is a local branch that is linked to a remote branch. When a tracking branch is pushed or pulled, it automatically pushes to or pulls from the remote branch that it is linked to. 

## Benefits

Tracking branches are very useful for keeping local branches up-to-date with remote branches. They also make it easier to collaborate with others since all changes can be tracked and merged with the remote branch. 

## Set Up

Tracking branches can be set up by using the `git branch --set-upstream-to` command. This command links the local branch to the remote branch and sets the tracking branch. 

## Usage

Once the tracking branch is set up, it can be used to push and pull changes to the remote branch. To push changes, use the `git push` command. To pull changes, use the `git pull` command.
