---
title: 0 1 1 * *
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: `0 1 1 * * ?`
---

**Contents**

[TOC]

### Section 1: 
Format: `0 1 1 * * ?`

### Section 2: 
Explanation: This cron expression will run a task at 1:01am every day. 

### Section 3: 
Breakdown: 
- Minute: `0`
- Hour: `1`
- Day of the Month: `1`
- Month: `*` (every month)
- Day of the Week: `*` (every day)
- Year: `?` (every year)

### Section 4: 
Example Usage: 
`@Scheduled(cron = "0 1 1 * * ?")`
