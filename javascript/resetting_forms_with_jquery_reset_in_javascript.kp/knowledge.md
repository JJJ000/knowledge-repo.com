---
title: Using jquery, how can a form be reset using the .reset() method?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The .reset() method can be used to reset a form using jQuery in Javascript.
---

**Contents**

[TOC]

# Section 1: Select the Form

The first step is to select the form you wish to reset. This can be accomplished using the jQuery selector. For example, if the form had an ID of "myForm", you could select it with the following code:

```javascript
var form = $("#myForm");
```

# Section 2: Reset the Form

Once the form has been selected, you can use the jQuery `.reset()` method to reset it. This method will reset all the form fields to their default values. The following code will reset the form:

```javascript
form.reset();
```

# Section 3: Refresh the Form

In some cases, you may want to refresh the form after resetting it. This can be done by calling the `.refresh()` method on the form. This will refresh the form and update any changes that have been made. The following code will refresh the form:

```javascript
form.refresh();
```

# Section 4: Submit the Form

Finally, if desired, you can submit the form after resetting and refreshing it. This can be done using the `.submit()` method. This will submit the form and any changes that have been made. The following code will submit the form:

```javascript
form.submit();
```
