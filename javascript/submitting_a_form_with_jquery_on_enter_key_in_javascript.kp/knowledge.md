---
title: Submitting a form using jquery when the 'enter' key is pressed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: $(`form`).on(`submit`, function(e) {e.preventDefault();});
---

**Contents**

[TOC]

### Step 1: Add Keyup Event Handler

Add a keyup event handler to the form element. Inside the event handler, check if the key pressed is the enter key.

```javascript
$("form").keyup(function(event){
    if(event.keyCode == 13){
        // code to execute when enter is pressed
    }
});
```

### Step 2: Prevent Default Action

Prevent the default action of the form submission when the enter key is pressed.

```javascript
$("form").keyup(function(event){
    if(event.keyCode == 13){
        event.preventDefault();
    }
});
```

### Step 3: Trigger Submit Event

Trigger the submit event on the form element when the enter key is pressed.

```javascript
$("form").keyup(function(event){
    if(event.keyCode == 13){
        event.preventDefault();
        $(this).trigger("submit");
    }
});
```

### Step 4: Add Submit Event Handler

Add a submit event handler to the form element. Inside the event handler, add the code to submit the form.

```javascript
$("form").keyup(function(event){
    if(event.keyCode == 13){
        event.preventDefault();
        $(this).trigger("submit");
    }
});

$("form").submit(function(){
    // code to submit the form
});
```
