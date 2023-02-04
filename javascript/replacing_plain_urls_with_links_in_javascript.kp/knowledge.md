---
title: What is the process for changing plain urls into links?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use regular expressions to search for plain URLs and replace them with HTML anchor tags.
---

**Contents**

[TOC]

#### Step 1: Identify the URLs

The first step in replacing plain URLs with links is to identify the URLs in the text. This can be done using a regular expression. The regular expression should look for strings that begin with "http" or "https" and end with a space or the end of the string.

#### Step 2: Create the Link

Once the URLs have been identified, the next step is to create a link for each URL. This can be done by creating a new string that contains the HTML link tag. The href attribute of the link should be set to the URL that was identified in the previous step.

#### Step 3: Replace the URL

The last step is to replace the plain URL with the link. This can be done by using the replace() method of the string. The first argument should be the plain URL and the second argument should be the HTML link tag that was created in the previous step.

#### Step 4: Test the Result

The final step is to test the result to make sure that the plain URL has been successfully replaced with a link. This can be done by testing the string with the new link in a web browser.
