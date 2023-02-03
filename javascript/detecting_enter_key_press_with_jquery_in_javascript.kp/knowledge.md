---
title: What is the jquery method for detecting a press of the enter key on the keyboard?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can detect pressing Enter on the keyboard using jQuery by binding a keyup event to the document and checking if the keycode is 13.
---

**Contents**

[TOC]

#### Using Keydown Event

The `keydown` event can be used to detect the pressing of the enter key. The following code snippet checks if the key pressed is the enter key, and then executes the code inside the `if` statement.

```javascript
$(document).keydown(function(e){
    if(e.which == 13){
        // Execute code here
    }
});
```

#### Using Keypress Event

The `keypress` event can also be used to detect the pressing of the enter key. The following code snippet checks if the key pressed is the enter key, and then executes the code inside the `if` statement.

```javascript
$(document).keypress(function(e){
    if(e.which == 13){
        // Execute code here
    }
});
```

#### Using Keyup Event

The `keyup` event can also be used to detect the pressing of the enter key. The following code snippet checks if the key pressed is the enter key, and then executes the code inside the `if` statement.

```javascript
$(document).keyup(function(e){
    if(e.which == 13){
        // Execute code here
    }
});
```

#### Using Form Submit

Forms can also be used to detect the pressing of the enter key. The following code snippet checks if the form is submitted, and then executes the code inside the `if` statement.

```javascript
$('form').submit(function(e){
    // Execute code here
});
```
