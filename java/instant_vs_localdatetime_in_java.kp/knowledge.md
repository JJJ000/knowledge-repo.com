---
title: What are the distinctions between instant and localdatetime?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Instant represents a moment on the timeline in UTC, while LocalDateTime represents a date-time without a time-zone in the ISO-8601 calendar system.
---

**Contents**

[TOC]

### Instant
Instant is a point in time on the timeline. It is an immutable object and is used to represent a specific moment in time that is independent of any particular calendar, time zone or locale.

### LocalDateTime
LocalDateTime is a date-time without any time zone information. It is an immutable object and is used to represent a specific moment in time that is relative to a particular calendar, time zone or locale.
