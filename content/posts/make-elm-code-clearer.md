---
title: "6 ways to make your Elm code clearer"
description: ""
tags: [ elm, software ]

date: 2022-01-16T16:27:42.000Z
---

Code clarity means less time fixing problems—especially in large codebases. But what habits are worth the effort? 

Here are 6 simple refactors to continually make to increase the clarity of your [Elm](https://twitter.com/elmlang) code:

### ✍️ Add type annotations

What data does a given function operate on?

Adding a type annotation answers this question, and makes Elm's compiler errors more accurate.

VS Code and IntelliJ both let you automatically generate annotations, making this easier.

### 🐜 Reduce function arguments to their minimum

Don't pass your entire `Model` to a function when it only needs a small subset.

Instead, use extensible record arguments, or pass data in separately.

This makes your functions easier to rule out as causes of errors when debugging.

### ↪️ Extract named functions

Sometimes you need complicated functions that involve multiple steps. But these can be hard to understand.

Extract each step into its own named functions, so that the complex function can be skimmed at a high level.

### 🌱 Move a type and its functions into a new module

Module interfaces are clearest when they focus on a single data type and its helper functions.

When you see new types and helper functions for then begin to show up, move them into their own module.

### 🎯 Rename modules accurately

Give your code a change to be findable when it's needed!

Make sure your modules are named for the types and helper functions they contain.

### 🚫 Move deprecated modules into a Deprecated directory

Are a module's types and functions the current "best practice" in your codebase? The answer isn't always clear.

Keep a `Deprecated` directory and move outdated modules there if they can't be removed yet.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1482751423255351302) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>