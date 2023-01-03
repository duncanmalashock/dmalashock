---
title: "Nested updates: an Elm antipattern"
description: ""
tags: [ elm, software ]

date: 2022-01-18T14:34:37.000Z
---

In [Elm](https://twitter.com/elmlang) it's hard to update nested records. Some people (including me) have complained about this.

A few years ago, I wrote some code to solve this "problem". Looking back, I wish I had approached it differently. 🧵

My clever solution was to write a shell script that let me write the "record-updater" function I wished I had, of the form:

`withUpdatedX` (where `X` is the field to update)

The script scanned for instances of these, and generated the corresponding functions in a module.

We started adopting this pattern because of its ease of use.

Our team grew, and I found myself explaining to others what these magical functions were and how to work with the script.

The usefulness wasn't usually worth the obscurity of the process.

There were two cases where we used these record-updater functions:

1) Updating nested records that model data (e.g. a `Subscription` with a `List Transaction`)

2) Passing record-updater functions as arguments (mostly for using a third-party library)

In the first case, I think the better option would be to model a `Subscription` as an opaque type, so that nested record updating was not possible.

Then we could design the `Subscription` module to include a helper function that made updating its `Transaction`s easier.

As for the second case, the "record-updater as an argument" interface has been a source of confusion in our codebase for some time because of its ergonomics in complex cases.

Generating the functions didn't make these cases any easier to understand.

One of the things I like about Elm's culture is that clever solutions like mine tend to seem like they might be a bad idea.

The design of the language encourages you to write in a simple and sensible way—stick to the patterns and chances are you'll have a maintainable program.

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1483447741233696769) as part of [Ship 30 for 30](https://www.ship30for30.com/).