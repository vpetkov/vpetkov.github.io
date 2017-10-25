---
layout: post
title:  "Keyboard Input in Full Screen Safari"
date:   2013-09-01 00:00:00 +0200
categories: Books
---

In most desktop browsers you can view any page in full screen. [Try it](javascript:document.documentElement.webkitRequestFullscreen();) (`ESC` stops it).

In macOS full screen was embraced system-wide after the success of the iPad. Similar to how iOS apps look full screen mode is a less distracting way to work on a single task. And especially valuable for small screens. Most apps on a Mac support full screen mode, including Safari. But there is a way to gain even more screen real estate for browsing - hiding all system UI completely. It's also particularly useful for presentations and screen-sharing.

In Safari full screen can be initiated by calling the `webkitRequestFullscreen()` method as I demonstrated above.

Actually the full screen functionality is meant for video. In [**Safari documentation**](https://developer.apple.com/library/content/documentation/AudioVideo/Conceptual/Using_HTML5_Audio_Video/ControllingMediaWithJavaScript/ControllingMediaWithJavaScript.html#//apple_ref/doc/uid/TP40009523-CH3-SW13) full screen is still listed under HTML5 Audio and Video.
Despite that it was possible to call the `webkitRequestFullscreen()` method with a flag `ALLOW_KEYBOARD_INPUT`. At least until September 2013.

The ability to accept alphanumeric keyboard events in full screen mode is considered a security risk by Apple. My best guess is that it could allow for websites to mimic system UI and in full screen to trick users into entering sensitive data.

The above mentioned documentation goes on to explain that the `webkitRequestFullscreen()` method can only be invoked in response to a user action, such as clicking a button. It cannot be invoked in response to a load event, for example.

This should solve any security concerns. But `ALLOW_KEYBOARD_INPUT` is no longer even mentioned in the documentation. It looks like the full screen functionality in Safari is after all intended to stay as part of HTML Audio and Video. Pitty because I think there are use cases calling for fully capable full screen API.

Curiously in [Safari Technology Preview](https://developer.apple.com/safari/technology-preview/) - Apple's beta version of Safari for developers keyboard input works in full screen without any flags needed to be passed.

It could just be one of those lingering issues in Apple's ecosystem. I've raised a couple of bugs about it. And I'm inviting everyone interested in the topic to help, comment, find solutions, and continue the discussion for proper full screen support.
