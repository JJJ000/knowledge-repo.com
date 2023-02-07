---
title: What is the expiration date for items stored in html5 local storage?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Items in HTML5 local storage do not expire unless they are manually removed.
---

**Contents**

[TOC]

# No Expiration

Items stored in HTML5 local storage do not expire. The data will remain in the storage until it is manually cleared or deleted.

# Manually Clearing Local Storage

Local storage can be cleared manually using the `localStorage.clear()` command. This will remove all items stored in the local storage.

# Deleting Items from Local Storage

Individual items can also be deleted from local storage using the `localStorage.removeItem(key)` command. This command takes a single argument, which is the key of the item to be deleted.

# Browser Settings

In some cases, browsers may allow users to set the expiration time for local storage items. This is usually done through the browser's settings menu. The expiration time is typically set in minutes, and any items stored after the expiration time will be removed from the local storage.
