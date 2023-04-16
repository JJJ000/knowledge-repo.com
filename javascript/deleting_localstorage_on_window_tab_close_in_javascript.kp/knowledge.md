---
title: What is the process for removing a localstorage item when the browser window/tab is closed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: LocalStorage items can be deleted when the browser window/tab is closed by using the `window.onbeforeunload` event.
---

**Contents**

[TOC]

1. Access the localStorage Object
2. Set an Event Listener 
3. Add an Event Handler 
4. Remove the localStorage Item 

## 1. Access the localStorage Object

The first step to deleting a localStorage item when the browser window/tab is closed is to access the localStorage object. This can be done by using the `window` object.

```javascript
const localStorage = window.localStorage;
```

## 2. Set an Event Listener 

The next step is to set up an event listener that will detect when the browser window/tab is closed. This can be done by using the `addEventListener()` method.

```javascript
window.addEventListener('beforeunload', () => {
    // code to delete localStorage item
});
```

## 3. Add an Event Handler 

Once the event listener has been set up, an event handler needs to be added. This is the code that will be executed when the browser window/tab is closed.

```javascript
const handleClose = () => {
    // code to delete localStorage item
};
```

## 4. Remove the localStorage Item 

Finally, the localStorage item needs to be removed. This can be done by using the `removeItem()` method on the localStorage object.

```javascript
localStorage.removeItem('key');
```
