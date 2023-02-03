---
title: Retrieve chosen option using jquery from dropdown menu
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The selected option from a dropdown can be retrieved using jQuery`s .val() method.
---

**Contents**

[TOC]

### 1. Using jQuery

```javascript
$("#dropdownID option:selected").text();
```

### 2. Using Javascript

```javascript
document.getElementById("dropdownID").value;
```

### 3. Using Vanilla JS

```javascript
document.querySelector('#dropdownID').value;
```

### 4. Using HTML DOM

```javascript
document.getElementById("dropdownID").options[document.getElementById("dropdownID").selectedIndex].text;
```
