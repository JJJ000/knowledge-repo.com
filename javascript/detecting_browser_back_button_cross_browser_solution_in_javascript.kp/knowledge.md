---
title: What is the best way to detect a browser back button event across different web browsers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Listen for the `popstate` event to detect a browser back button event in a cross-browser compatible way.
---

**Contents**

[TOC]

## Section 1: Using the Popstate Event
The `popstate` event is fired when the active history entry changes. This event is fired when the user navigates through the history, either by clicking back or forward in the browser, or by calling `history.back()` or `history.forward()`.

## Section 2: Using the Hash Change Event
The `hashchange` event is fired when the fragment identifier of the URL has changed. This event is fired when the user navigates through the history, either by clicking back or forward in the browser, or by calling `history.back()` or `history.forward()`.

## Section 3: Using the Beforeunload Event
The `beforeunload` event is fired when the window, the document and its resources are about to be unloaded. This event can be used to detect the browser back button and can be used to prevent the user from leaving the page.

## Section 4: Using the Unload Event
The `unload` event is fired when the document or a child resource is being unloaded. This event can be used to detect the browser back button and can be used to prevent the user from leaving the page.
