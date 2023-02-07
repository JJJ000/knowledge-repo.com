---
title: What is the best way to save different information for html elements?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Data can be stored as custom attributes on HTML tags using the `data-` prefix.
---

**Contents**

[TOC]

# Section 1: Using HTML5 Data Attributes

One way to store arbitrary data for HTML tags in Javascript is to use HTML5 data attributes. These are custom attributes that start with "data-" and can be used to store any kind of data. For example, if you wanted to store a user's name in an HTML tag, you could use the following syntax:

```html
<div data-user="John Doe">...</div>
```

# Section 2: Accessing the Data

Once you have set the data attributes, you can access them in Javascript using the `dataset` property. This property contains an object with all of the HTML5 data attributes that have been set on the element. For example, to access the user's name from the previous example, you could use the following code:

```javascript
var userName = document.querySelector('div').dataset.user;
```

# Section 3: Updating the Data

You can also update the data attributes using the `dataset` property. For example, if you wanted to update the user's name, you could use the following code:

```javascript
document.querySelector('div').dataset.user = 'Jane Doe';
```

# Section 4: Removing the Data

Finally, you can also remove the data attributes by setting the value to `null`. For example, to remove the user's name from the previous example, you could use the following code:

```javascript
document.querySelector('div').dataset.user = null;
```
