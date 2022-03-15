---
layout: post
title: Flutter - Reasons Why You Will Fall In Love With It
description: Google’s SDK is here, and it has a word to say in Mobile App development
summary: Google’s SDK is here, and it has a word to say in Mobile App development.
tags: coding
minute: 2
---

At first sight, this may seem the name of some kind of butterfly, but it is **Google’s new framework for building high-quality native apps** for iOS and Android. If you’re a Mobile Developer, you should take a look at it as it’s going to change the way native apps are developed.

## Code once, run anywhere

With Flutter, you can code one time and run the same app for iOS and Android devices, and it’ll automatically adapt to each operative system.

You’re probably thinking _“What if I want to have different stuff on each device?”._ — You can! Flutter gives you the possibility to adapt the code and UI of the app depending on which devices are being run.

```dart
    theme: new ThemeData(
    primaryColor:
        Theme.of(context).platform == Target.Platform.iOS
        ? Colors.grey[100]
        : Colors.blue
    )
```

The above code changes the theme color to grey if the device used is running iOS and blue if it’s an Android device.

### The Usain Bolt Of Mobile App Development

![](https://media.giphy.com/media/F0qo2FvhGIbXG/giphy.gif)

Everything is fast when using Flutter, from code writing to compiling.

If you want to build an app as fast as possible without much complication you’ve found your way.

## UI Code

The simplicity remains in how you only need one language for the whole app. Forget a huge load of files created when developing using Android Native.

> Flutter’s widget is written in Dart language. So you have everything in the same file, without having to keep switching files to modify the UI and its functionality.

The downside is the **deeply nested code** that you’ll need to write and edit when using Flutter.

Moreover, when I say deeply nested code, _I really mean it_! Imagine all the conditionals, transformations, iterations, state reading, event handlers and the UI in the same functions.

_I know, right?_

This makes it **unusable when you start** working with it but gets easier as you start using it.

## Hot Reload

Besides that, Flutter has the fantastic **Hot Reload** feature that is a fast Dart Compiler technology that allows you to load code changes into a running app without losing its actual state. The changes are applied **instantly** in the running app.

### It’s not just fun and games

Flutter Beta 2 was announced in April 2018, and there is no stable version yet. Which means that there’ll be changes and improvements that may demand changes on your code.

Yes, it’s true that Google’s support to Flutter is impressive but, despite this fact, the amount of libraries available to be used with Flutter is still low. It would be very time-consuming for the developers to build the necessary libraries, which ultimately kills the primary purpose of Flutter.

However there’s more…

## Dart…

To develop Flutter apps, you’ll need to learn Dart or hire a Dart developer. It’s really not a hard thing to learn, and if you’re a developer you might like to learn as many languages as possible, but maybe you’ll lose some time trying to get used to it.

### Is it worth it?

Flutter is fun and fast to code a well-designed app. Still has much room to improve to become a real opponent to Android Native.

For a reasonably modern framework, Flutter has progressed remarkably quick and, surely it will have a word to say in the future for the Mobile App development.

_Is it ready to be applied to big scale apps?_ Likely not, but I’m expecting after these things are fixed, **we can all enjoy Flutter!**

> Well, folks, that is all for now!

This Blog Post was written during my internship at [PICUS](https://picuscreative.com/).