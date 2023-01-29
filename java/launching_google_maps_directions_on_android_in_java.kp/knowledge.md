---
title: Triggering a google maps directions request on Android using an intent
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: An intent can be used to launch Google Maps Directions by setting the action to ACTION\_VIEW and the URI to a valid directions intent URL.
---

**Contents**

[TOC]

### Creating the Intent

The following code snippet creates an intent to launch Google Maps Directions.

```java
Intent intent = new Intent(android.content.Intent.ACTION_VIEW, 
 Uri.parse("http://maps.google.com/maps?saddr=20.344,34.34&daddr=20.5666,45.345"));
startActivity(intent);
```

### Setting the Start and End Locations

The `saddr` parameter in the URL specifies the start location, while the `daddr` parameter specifies the end location. The coordinates of the start and end locations must be specified in latitude and longitude format.

### Adding Waypoints

It is possible to add waypoints to the route by adding the `waypoints` parameter to the URL. The waypoints must be specified in the same format as the start and end locations, and multiple waypoints can be added by separating them with a `|` character.

### Launching the Intent

Once the intent has been created, it can be launched by calling the `startActivity()` method, passing it the intent object. This will launch the Google Maps Directions app with the specified start and end locations, and any waypoints that have been added.
