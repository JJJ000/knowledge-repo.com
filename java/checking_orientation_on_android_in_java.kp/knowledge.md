---
title: Verify the orientation settings on an Android device
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To check the orientation on an Android phone in Java, use the getOrientation() method of the Display class.
---

**Contents**

[TOC]

### Step 1: Detect Sensor

To detect the orientation of an Android phone in Java, the first step is to detect the sensor. In order to do this, the following code can be used:

```java
SensorManager sensorManager = (SensorManager) getSystemService(Context.SENSOR_SERVICE);
Sensor accelerometer = sensorManager.getDefaultSensor(Sensor.TYPE_ACCELEROMETER);
```

### Step 2: Register Listener

Once the accelerometer sensor is detected, a listener needs to be registered to it. This can be done with the following code:

```java
sensorManager.registerListener(this, accelerometer, SensorManager.SENSOR_DELAY_NORMAL);
```

### Step 3: Get Sensor Data

Once the listener is registered, the onSensorChanged() method will be called whenever the sensor data changes. This method will receive a SensorEvent object which contains the sensor data as follows:

```java
public void onSensorChanged(SensorEvent event) {
 float x = event.values[0];
 float y = event.values[1];
 float z = event.values[2];
}
```

### Step 4: Determine Orientation

Finally, the orientation of the device can be determined by comparing the values of x, y and z. If x is greater than y and z, the device is in landscape mode. If y is greater than x and z, the device is in portrait mode.
