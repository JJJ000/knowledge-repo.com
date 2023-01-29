---
title: Example of an alarm manager
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: AlarmManager can be used to schedule an Intent to be executed at a specified time in the future.
---

**Contents**

[TOC]

1. Overview
An Alarm Manager is a utility class in Java that allows developers to schedule tasks to be executed at a specific time or after a specific delay. It is used to set alarms that can be used to trigger events at a specific time or after a specific delay. It is a powerful tool for scheduling tasks and managing alarms in an application.

2. Implementation
The Alarm Manager can be implemented using the following steps:

Step 1: Create an instance of the AlarmManager class.

Step 2: Create a PendingIntent that will be used to trigger the alarm.

Step 3: Set the alarm by calling the set() method of the AlarmManager class.

Step 4: Register a BroadcastReceiver to receive the alarm intent.

Step 5: Handle the alarm intent in the BroadcastReceiver.

3. Example
The following example shows how to use the AlarmManager to trigger an alarm every 10 seconds.

// Create an instance of the AlarmManager
AlarmManager alarmManager = (AlarmManager) getSystemService(Context.ALARM_SERVICE);

// Create a PendingIntent to trigger the alarm
Intent intent = new Intent(this, AlarmReceiver.class);
PendingIntent pendingIntent = PendingIntent.getBroadcast(this, 0, intent, 0);

// Set the alarm to trigger every 10 seconds
alarmManager.setRepeating(AlarmManager.RTC_WAKEUP, System.currentTimeMillis(), 10 * 1000, pendingIntent);

4. Conclusion
The Alarm Manager is a powerful tool for scheduling tasks and managing alarms in an application. It is easy to use and can be used to trigger events at a specific time or after a specific delay.
