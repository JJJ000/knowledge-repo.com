---
title: Can I substitute my own dialog for the onbeforeunload dialog?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can replace the OnBeforeUnload dialog with your own by setting the window.onbeforeunload event handler.
---

**Contents**

[TOC]

1. Obtain User Consent
Before attempting to override the OnBeforeUnload dialog, it is important to obtain user consent. The user should be made aware that their experience on the page may be altered by the override and given the option to accept or reject the change.

2. Override OnBeforeUnload Dialog
The OnBeforeUnload dialog can be overridden by setting the `window.onbeforeunload` property to a custom function. This function should return a string that will be displayed in the dialog.

3. Create Custom Dialog
The custom dialog should be created using HTML and CSS. It should contain a message informing the user of the action they are about to take and two buttons, one to accept the action and one to cancel it.

4. Attach Event Listeners
Event listeners should be attached to the two buttons in the custom dialog. The 'accept' button should trigger the action the user is attempting to take, while the 'cancel' button should close the dialog and return the user to the page.
