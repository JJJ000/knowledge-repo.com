---
title: The difference between 'addeventlistener' and 'onclick' in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: addEventListener allows you to add multiple event handlers for an element, whereas onclick only allows one.
---

**Contents**

[TOC]

**Event Listeners**

Event Listeners are functions that are triggered when a certain event occurs. They are used to listen for events, such as a user clicking a button or hovering over an element, and then execute a specific action in response. The event listener is attached to an element and will remain attached until it is removed.

**addEventListener**

addEventListener is a method used to add an event listener to an element. It takes two arguments: the event type and the event handler. The event type is the type of event that will trigger the event listener, such as "click" or "mouseover". The event handler is the function that will be executed when the event type occurs.

**onclick**

onclick is an attribute that is added to an element to specify what function should be executed when the element is clicked. It is a shorthand for adding an event listener for the "click" event type.

**Comparison**

addEventListener and onclick are both used to add an event listener to an element, but they differ in how they are used. addEventListener is a method that takes two arguments, while onclick is an attribute that can only be used to specify a single function. addEventListener is more versatile, as it can be used to add event listeners for any type of event, while onclick is limited to only the "click" event type.
