---
title: Determining the client's time zone and offset in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The client`s time zone and offset can be retrieved using the Date.getTimezoneOffset() method.
---

**Contents**

[TOC]

# Using the Date Object

The Date object can be used to get the current time zone offset of the client's browser.

```javascript
let offset = new Date().getTimezoneOffset();
```

This will return the time zone offset in minutes. To convert this to hours, divide the offset by 60.

# Using the Intl Object

The Intl object can be used to get the current time zone of the client's browser.

```javascript
let timezone = Intl.DateTimeFormat().resolvedOptions().timeZone;
```

This will return the IANA time zone name of the client's browser.

# Using the Geolocation API

The Geolocation API can be used to get the current location of the client's browser.

```javascript
navigator.geolocation.getCurrentPosition((position) => {
    let lat = position.coords.latitude;
    let lon = position.coords.longitude;
});
```

This will return the latitude and longitude of the client's browser. These can then be used to get the time zone of the client.
