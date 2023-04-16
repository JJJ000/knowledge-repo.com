---
title: Include a tooltip within a div element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `title` attribute to add a tooltip to a div in Javascript.
---

**Contents**

[TOC]

**Step 1: Add HTML Element**

First, add an HTML element to the div you want to add a tooltip to. This element should have an `id`, `title` and `data-toggle` attribute.

```html
<div id="example-div" title="This is a tooltip" data-toggle="tooltip">
  Example div content
</div>
```

**Step 2: Add CSS Styling**

Next, add some CSS styling to the tooltip element. This will determine how the tooltip looks and behaves when it is displayed.

```css
#example-div[data-toggle="tooltip"] {
  position: relative;
  display: inline-block;
}

#example-div[data-toggle="tooltip"]::before {
  content: attr(title);
  position: absolute;
  top: 0;
  left: 0;
  background: #000;
  color: #fff;
  padding: 0.5rem;
  border-radius: 0.25rem;
  opacity: 0;
  transition: opacity 0.2s;
}

#example-div[data-toggle="tooltip"]:hover::before {
  opacity: 0.8;
}
```

**Step 3: Add Javascript**

Finally, add some Javascript to initialize the tooltip. This will allow the tooltip to be displayed when the user hovers over the div.

```javascript
const exampleDiv = document.getElementById('example-div');

exampleDiv.addEventListener('mouseover', () => {
  exampleDiv.setAttribute('data-toggle', 'tooltip');
});
```

**Step 4: Test Tooltip**

Once all the steps are complete, test the tooltip to make sure it is working correctly. Hover over the div to check that the tooltip is displayed correctly.
