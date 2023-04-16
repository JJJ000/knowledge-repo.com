---
title: What is the purpose of jquery's $(document).ready and updatepanels?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery $(document).ready can be used to execute code after an UpdatePanel has finished loading in Javascript.
---

**Contents**

[TOC]

# jQuery $(document).ready

jQuery $(document).ready is a function that is used to execute a function when the DOM (Document Object Model) is fully loaded. It is important to use this function to ensure that the code is executed only after the DOM is ready. This helps to avoid any errors that may occur due to the code being executed before the DOM is ready.

# UpdatePanels in Javascript

UpdatePanels are a feature of ASP.NET AJAX which allow for partial page updates without reloading the entire page. This helps to improve the user experience by reducing the amount of time it takes for the page to load. UpdatePanels can be used to update specific parts of the page without reloading the entire page. This is done by using JavaScript to send an AJAX request to the server, which then sends back the updated HTML content to the browser. The browser then updates the page with the new content.
