---
title: View the actual time and date of a commit on github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: GitHub displays the date and time of each commit in the local timezone of the user viewing the repository.
---

**Contents**

[TOC]

## Date Format

In GitHub, the date and time of a commit is displayed in the ISO 8601 format (YYYY-MM-DDTHH:MM:SSZ). This format includes the year, month, day, hour, minute, and second of the commit.

## Time Zone

The time zone of the commit is always displayed in UTC (Coordinated Universal Time). This is the same time zone used by GitHub for all its timestamps.

## Viewing Commit Date/Time 

The date and time of a commit can be viewed on the commit page for the commit. This page can be accessed by clicking on the commit hash next to the commit message on the repository page.

## Changing Date/Time Format

The date and time of a commit cannot be changed in GitHub. However, users can use the command line to view the commit date/time in a different format. For example, the `git log` command can be used to view the commit date/time in the local time zone.
