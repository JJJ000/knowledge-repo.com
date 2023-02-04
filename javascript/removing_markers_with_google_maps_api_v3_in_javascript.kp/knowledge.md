---
title: What is the process for deleting all markers from the google maps API v3?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `clearMarkers()` method on the Google Maps MarkerClusterer instance.
---

**Contents**

[TOC]

## Section 1: Get all markers

In order to remove all markers, you first need to get a list of all markers that are currently on the map. This can be done by looping through the `map.markers` array, which contains all the markers that have been added to the map.

## Section 2: Remove markers

Once you have a list of all the markers, you can use the `remove()` method on each marker to remove it from the map. This can be done by looping through the list of markers and calling `remove()` on each one.

## Section 3: Clear markers array

Once all the markers have been removed from the map, you will need to clear the `map.markers` array. This can be done by setting the array to an empty array using the `map.markers = []` command.

## Section 4: Reset map

Finally, you will need to reset the map to ensure that all markers are removed from the map. This can be done by calling the `map.reset()` method. This will reset the map and remove all markers from the map.
