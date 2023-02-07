---
title: What zoom level should be set on the map to display all visible markers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the map`s fitBounds() method to set the zoom of the map to cover all visible markers.
---

**Contents**

[TOC]

## Section 1 - Create Bounds

The first step is to create a bounds object that contains all of the visible markers. This can be done by looping through each marker and extending the bounds object to include the marker's coordinates.

```javascript
// Create bounds object
var bounds = new google.maps.LatLngBounds();

// Loop through markers
for (var i = 0; i < markers.length; i++) {
  bounds.extend(markers[i].getPosition());
}
```

## Section 2 - Set Map Zoom

Once the bounds object has been created, the map's zoom can be set to cover all of the markers using the `fitBounds()` method.

```javascript
// Set map zoom to cover all markers
map.fitBounds(bounds);
```

## Section 3 - Listen for Zoom Change

The `fitBounds()` method will set the map's zoom to the minimum zoom level that covers all of the markers. In some cases, this may be too zoomed out and the user may want to zoom in further. To allow for this, an event listener can be added to listen for changes in the map's zoom level.

```javascript
// Listen for zoom change
google.maps.event.addListener(map, 'zoom_changed', function() {
  // Do something
});
```

## Section 4 - Limit Maximum Zoom

To prevent the user from zooming in too far, a maximum zoom level can be set. This can be done by checking the map's current zoom level in the event listener and setting a maximum zoom level. If the zoom level is higher than the maximum, the zoom level can be set to the maximum.

```javascript
// Listen for zoom change
google.maps.event.addListener(map, 'zoom_changed', function() {
  // Get current zoom level
  var zoom = map.getZoom();
  
  // Set maximum zoom level
  var maxZoom = 12;
  
  // Check zoom level
  if (zoom > maxZoom) {
    // Set zoom level to maximum
    map.setZoom(maxZoom);
  }
});
```
