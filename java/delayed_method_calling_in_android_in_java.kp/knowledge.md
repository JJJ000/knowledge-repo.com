---
title: What is the best way to call a method after a delay in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Handler class to post a Runnable that calls the desired method after the desired delay.
---

**Contents**

[TOC]

1. **Using Handler**

A Handler allows you to send and process Message and Runnable objects associated with a thread's MessageQueue.

To call a method after a delay using Handler:

- Create a Handler instance
- Create a Runnable instance
- Post the Runnable to the Handler with a delay
- In the Runnable, call the method

```java
Handler handler = new Handler();
Runnable runnable = new Runnable() {
    @Override
    public void run() {
        // Call your method here
    }
};

handler.postDelayed(runnable, 1000); // 1 second delay
```

2. **Using Timer**

A Timer allows you to schedule a task to be executed at a certain time or periodically.

To call a method after a delay using Timer:

- Create a Timer instance
- Create a TimerTask instance
- Schedule the TimerTask with a delay
- In the TimerTask, call the method

```java
Timer timer = new Timer();
TimerTask timerTask = new TimerTask() {
    @Override
    public void run() {
        // Call your method here
    }
};

timer.schedule(timerTask, 1000); // 1 second delay
```

3. **Using CountDownTimer**

A CountDownTimer is a subclass of the Timer class that allows you to schedule a task to be executed after a certain amount of time has elapsed.

To call a method after a delay using CountDownTimer:

- Create a CountDownTimer instance
- Override the onTick and onFinish methods
- In the onFinish method, call the method

```java
CountDownTimer countDownTimer = new CountDownTimer(1000, 1000) {
    @Override
    public void onTick(long millisUntilFinished) {
        // Do something at each tick
    }

    @Override
    public void onFinish() {
        // Call your method here
    }
};

countDownTimer.start(); // 1 second delay
```

4. **Using Thread**

A Thread allows you to execute code in a separate thread of execution.

To call a method after a delay using Thread:

- Create a Thread instance
- Override the run method
- In the run method, call the method after a delay

```java
Thread thread = new Thread() {
    @Override
    public void run() {
        try {
            Thread.sleep(1000); // 1 second delay
            // Call your method here
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
};

thread.start();
```
