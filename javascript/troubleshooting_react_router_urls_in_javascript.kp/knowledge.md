---
title: When attempting to manually refresh a page or type in a react-router url, the page will not load correctly
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: React-router URLs rely on the browser`s history API, so they will not work when refreshing or writing manually.
---

**Contents**

[TOC]

**Section 1: React-Router URLs**

React-Router URLs are URLs that are used with React-Router, a popular routing library for React applications. React-Router URLs are designed to be used with the React-Router library to enable routing within a React application. They are based on the HTML5 History API, and they enable developers to create single-page applications that are able to respond to changes in the URL without reloading the page.

**Section 2: Refreshing React-Router URLs**

When a React-Router URL is refreshed, the browser will attempt to reload the page. However, since React-Router URLs are based on the HTML5 History API, the browser will not be able to find the page and will return a "Page Not Found" error. This is because the page is not actually stored on the server, but instead is generated dynamically by React-Router.

**Section 3: Writing React-Router URLs Manually**

When writing React-Router URLs manually, the browser will not be able to find the page and will return a "Page Not Found" error. This is because the page is not actually stored on the server, but instead is generated dynamically by React-Router. To successfully navigate to a React-Router URL, it must be entered into the browser's address bar, not manually typed into the URL string.

**Section 4: Solution**

The solution to this issue is to use the React-Router library to create a link to the desired page. This will enable the browser to correctly find the page and load it, without returning a "Page Not Found" error. Additionally, if the React-Router URL is manually entered into the browser's address bar, it will still be able to find the page and load it correctly.
