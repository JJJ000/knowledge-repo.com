---
title: What is the proper way to show a confirmation message when an <a> link is clicked?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Call a JavaScript confirm() function when the <a> link is clicked.
---

**Contents**

[TOC]

**Section 1: Create the HTML Link**

In order to display a confirmation dialog when clicking an `<a>` link, we must first create the link itself. This can be done by using the following HTML code:

```html
<a href="#" onclick="return confirm('Are you sure?')">Click Here</a>
```

**Section 2: Add the Javascript Function**

Next, we must add the Javascript function that will be triggered when the link is clicked. This can be done by using the following code:

```javascript
function confirmLink() {
  return confirm('Are you sure?');
}
```

**Section 3: Add the onclick Event**

Finally, we must add the `onclick` event to the link so that the Javascript function is triggered when the link is clicked. This can be done by using the following code:

```html
<a href="#" onclick="return confirmLink()">Click Here</a>
```

**Section 4: Test the Link**

At this point, the link should now be set up to display a confirmation dialog when clicked. To test it, simply click the link and you should see the confirmation dialog appear.
