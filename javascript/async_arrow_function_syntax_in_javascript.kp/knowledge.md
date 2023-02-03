---
title: The syntax for an asynchronous arrow function is 
async () => { 
  // code here 
}
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: An async arrow function is defined as `async () => { // code here }`.
---

**Contents**

[TOC]

# Syntax
`async` function `name`(`parameter`) {
   `statement`
}

# Example
async function getData() {
   const response = await fetch('https://example.com/data');
   const data = await response.json();
   console.log(data);
}

# Arrow Function
async (parameter) => {
   `statement`
}

# Example
const getData = async (url) => {
   const response = await fetch(url);
   const data = await response.json();
   console.log(data);
}
