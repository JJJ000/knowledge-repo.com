---
title: What is the best way to use anchor hash linking in angularjs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: AngularJS provides the $location service to handle anchor hash linking.
---

**Contents**

[TOC]

1. **Setting up the Routes**

In order to handle hash linking in AngularJS, you will need to set up the routes in the `$routeProvider`, which is the core of AngularJS routing. The `$routeProvider` allows you to set up routes that will be triggered when a user navigates to a certain URL. You can also set up routes that will be triggered when a user clicks on an anchor hash link.

2. **Using the `$location` Service**

Once you have set up the routes, you can use the `$location` service to handle the hash linking. The `$location` service provides methods for getting and setting the URL fragment, which is what is used for hash linking. You can use the `$location.hash()` method to get the current URL fragment and the `$location.hash(hash)` method to set the URL fragment.

3. **Handling the Hash Link Click**

When a user clicks on an anchor hash link, you will need to handle the click event and call the `$location.hash()` method with the hash value from the link. This will set the URL fragment to the hash value, which will then trigger the appropriate route.

4. **Updating the Browser URL**

Once the route has been triggered, you may also want to update the browser URL to reflect the new URL fragment. You can do this by calling the `$location.url()` method with the new URL. This will update the browser URL to the new URL, which will then be reflected in the browser address bar.
