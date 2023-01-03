---
title: "Well-designed modules in Elm"
description: ""
tags: [ elm, software ]

date: 2022-01-24T17:24:11.000Z
---

What is a "well-designed" module in [Elm](https://twitter.com/elmlang)?

How can we design modular interfaces to be clear, understandable, and strong?

Here are a few guidelines:

### 🧥 Don't expose everything

A good module interface is intentional. So don't use `exposing (..)`. 

Choose what should be exposed, and what shouldn't.

### ☝️ Start with a type

Your module should be named after the type it's "about". 

For instance, a `Calendar.elm` module should be about a `Calendar` datatype and its associated helper functions.

### 🧳 Avoid exposing all variants of a type

If client code is able to destructure your type or use variants directly, your interface will be less durable.

There are exceptions, but as a general rule, instead of `Calendar(..)`, provide your interface through functions.

### 🎯 Functions should relate to your central type

If you find yourself writing functions prefixed with another type's name (e.g. `monthToString`, `monthFromDate`), this is a likely sign that these belong with the `Month` type in in a new module.

### 🧠 Take advantage of conventions

Interfaces are forms of communication—be consistent with conventions that users of your code are likely to know!

For instance, In Elm, models are usually named `Model`, are initialized with an `init` function, updated with `update`, etc.

### 🍱 Organize with doc comments

Organizing your exposed types in logical groupings is a great way to help your code's users get their bearings before they read the documentation.

`elm-format` arranges your exposures accordingly when you use `@docs` in your doc-comments.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1485664744216444932) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>