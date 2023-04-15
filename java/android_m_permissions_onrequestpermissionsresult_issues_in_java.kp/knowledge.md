---
title: Troubleshooting the issue of 'onrequestpermissionsresult()' not triggering in Android m permissions
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The onRequestPermissionsResult() method should be overridden in the Activity or Fragment that requested the permission.
---

**Contents**

[TOC]

### Overview
Android M introduced a new set of permissions for applications that target API level 23 and above. This new permission model requires applications to request permissions from users at runtime, rather than at install time. This is done via the onRequestPermissionsResult() callback, which is called when the user grants or denies a permission request. However, many developers have reported that onRequestPermissionsResult() is not being called in their Java code. 

### Possible Causes
There are several possible causes for this issue. The most common is that the permissions are not being requested properly. The onRequestPermissionsResult() callback will only be called if the permission request is made correctly. If the request is not made correctly, the callback will not be triggered. 

Another possible cause is that the user has already granted the permission. If the user has already granted the permission, the onRequestPermissionsResult() callback will not be called. 

Finally, the issue could be related to the Android version. The onRequestPermissionsResult() callback was introduced in API level 23, so it will not be available on devices running older versions of Android. 

### Solutions
The best way to solve this issue is to ensure that the permissions are being requested correctly. This can be done by using the requestPermissions() method, which is available in API level 23 and above. The method should be called with an array of permissions and a request code. The request code is used to identify the request, and the callback will be triggered with the same request code. 

If the user has already granted the permission, it is best to check the result of the requestPermissions() call before making the request. This can be done by calling the shouldShowRequestPermissionRationale() method, which will return true if the user has already granted the permission. 

Finally, it is important to ensure that the application is targeting API level 23 or higher. If the application is targeting an older version of Android, the onRequestPermissionsResult() callback will not be available.
