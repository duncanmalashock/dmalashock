---
title: "Hard in Elm: dropdown menus"
description: ""
tags: [ elm, software ]

date: 2022-02-14T14:04:21.000Z
---

Implementing a dropdown menu in [Elm](https://twitter.com/elmlang) is an unexpectedly deep topic!

Here are a few challenges you may run into:

### 1️⃣ Closing on click-away

One of the first issues you'll run into is how to close the menu in response to a click elsewhere on the page.

Otherwise, you'll have a dropdown menu that can only be closed by clicking on the toggle that opened it.

Global click handlers can be attached to the application as subscriptions. 

Since choosing a menu option should close the menu, a global click subscriptions can produce a separate Msg that closes the menu.

### 2️⃣ Allowing clicks inside the menu

If your dropdown menu is designed to allow further click interactions inside the menu pane, the previous solution won't work.

You need a way for your global click Msg to determine whether the click was inside the menu or not.

This can be done in pure Elm by decoding the click event to find HTML attributes of its target, but it is complex!

It can also be done in JS with a web component or a port.

### 3️⃣ Making the menu visible above scrolling content

In CSS, scrolling containers have their overflow clipped. In cases where your dropdown is in a scrolling container, your menu may be partially hidden.

One solution to this problem is to ensure the menu is always rendered at a higher part of the DOM tree, where it is sure to be visible.

A solution like this needs to query for the intended size and positioning of the menu, because relative positioning will not be possible.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1493224595863842824) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>