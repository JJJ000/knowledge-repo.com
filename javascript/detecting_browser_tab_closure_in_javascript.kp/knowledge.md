---
title: Determine if a web browser or tab is being closed
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The `onbeforeunload` event can be used to detect browser or tab closing in Javascript.
---

**Contents**

[TOC]

## Using the onbeforeunload Event 

The `onbeforeunload` event can be used to detect browser or tab closing. This event is triggered when a document is about to be unloaded. This event can be used to show a confirmation box to the user to verify if they want to leave the page or stay on the page.

## Event Handler

The `onbeforeunload` event can be handled using an event listener. The event listener is used to listen for the `onbeforeunload` event and call a function when the event is triggered. The function that is called can be used to show a confirmation box to the user.

## Confirmation Box

The confirmation box can be used to ask the user if they want to stay on the page or leave the page. The user can then choose to stay on the page or leave the page. This can be used to detect if the user is closing the browser or tab.

## Return Value

The `onbeforeunload` event can also be used to return a value. The value that is returned can be used to determine if the user is closing the browser or tab. If the user is closing the browser or tab, the value returned will be `true`. If the user is not closing the browser or tab, the value returned will be `false`.
