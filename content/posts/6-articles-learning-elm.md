---
title: "6 timeless articles about learning Elm"
description: ""
tags: [ elm, software ]

date: 2022-01-09T16:15:48.000Z
---

Learning [Elm](https://twitter.com/elmlang)? When I started learning it in 2016, [Joël Quenneville](https://twitter.com/joelquen)'s technical writing was a huge resource—and it still is.

Joël's clear, well-reasoned writing explains how to solve common issues and leverage Elm's type system.

Here are 6 timeless articles from Elm's "Coach Q":

### ✅ Booleans and Enums

[https://thoughtbot.com/blog/booleans-and-enums](https://thoughtbot.com/blog/booleans-and-enums)

If you come from languages that don't have union types, it's natural to reach for the familiar `Bool` and `String` types to model your data.

In Elm, we can do better! Joël uses concrete, clear examples to show us how.

### ⚙️ Maybe Mechanics

[https://thoughtbot.com/blog/maybe-mechanics](https://thoughtbot.com/blog/maybe-mechanics)

Elm makes certain bugs impossible by making you declare a nullable value explicitly. 

But knowing when and how to use the `Maybe` type is its own skill. Joël explains clearly what to do in the most common situations.

### ⚖️ Problem Solving with Maybe

[https://thoughtbot.com/blog/problem-solving-with-maybe](https://thoughtbot.com/blog/problem-solving-with-maybe)

`Maybe` is useful, but using it for each instance of a nullable value can overwhelm your codebase.

Joël shows how to make maintenance easier and how to model for more clarity.

### 😵‍💫 What's Weird with Maybe List

[https://thoughtbot.com/blog/whats-weird-with-maybe-list](https://thoughtbot.com/blog/whats-weird-with-maybe-list)

Combining `Maybe` with types that have their own null states can make your program states ambiguous.

Joël provides helpful alternatives and makes a case for when `Maybe (List a)` is useful.

### 🎲 Rolling Random Romans

[https://thoughtbot.com/blog/rolling-random-romans](https://thoughtbot.com/blog/rolling-random-romans)

Generating random values in Elm is a challenging beginner topic. How do you produce random values when all functions are pure?

Joël helps introduce the `Generator` type and breaks the problem down into simple steps.

### 🪲 Debugging DOM event handlers in Elm 

[https://thoughtbot.com/blog/debugging-dom-event-handlers-in-elm](https://thoughtbot.com/blog/debugging-dom-event-handlers-in-elm)

Elm's helpful constraints make web development easier. But debugging the boundary between JavaScript and Elm (e.g. decoding JSON values) can be confusing.

Joël shares helpful tips for "seeing into" decoders.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1480211715774107651) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>