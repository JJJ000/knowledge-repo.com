---
title: Button in html to prevent form from being submitted
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `type=`button`` attribute on the HTML button element to prevent the form from submitting when clicked.
---

**Contents**

[TOC]

### Prevent Default Behavior

The simplest way to stop a form from submitting is to use the `preventDefault()` method. This method prevents the default behavior of the form. This can be done by adding an `event listener` to the form, and then calling `preventDefault()` when the submit event is triggered.

```js
document.querySelector('form').addEventListener('submit', function(event) {
  event.preventDefault();
});
```

### Return False

Another way to stop a form from submitting is to return `false` from the `onSubmit` event handler. This will prevent the form from being submitted.

```js
<form onsubmit="return false;">
  ...
</form>
```

### Use a Button

Instead of using an `input` element with a `type="submit"`, use a `button` element instead. This will prevent the form from being submitted, as the `button` element does not have a `submit` behavior by default.

```html
<form>
  <button type="button">Submit</button>
</form>
```

### Disable the Submit Button

Finally, you can disable the submit button to prevent the form from being submitted. This can be done by setting the `disabled` attribute on the submit button.

```html
<form>
  <input type="submit" disabled>
</form>
```
