---
title: "2 \"builder\" patterns in Elm"
description: ""
tags: [ elm, software ]

date: 2022-01-30T15:42:01.000Z
---

[Elm](https://twitter.com/elmlang) has two very common design patterns that both use pipeline function application.

Confusingly, both of them are commonly called the "builder" pattern!

Here's what they are, how to tell them apart, and when to use them:

🎛 Builder #1 for optional data with defaults

The first pattern is an interface for configuring data with optional values. 

`Button.newArgs` initializes a `Button.Args` with defaults:
[https://sporto.github.io/elm-patterns/basic/builder-pattern.html](https://sporto.github.io/elm-patterns/basic/builder-pattern.html)

This allows the user to set optional values by applying functions.

Builder #1 is commonly used:
- in UI code
- when optional configuration would make a function signature too cumbersome without it

🔧 Builder #2 for constructing a type piece by piece

The second pattern wraps a constructor function whose arguments are gradually applied by successive function calls.

Example:
[https://sporto.github.io/elm-patterns/advanced/pipeline-builder.html](https://sporto.github.io/elm-patterns/advanced/pipeline-builder.html)

Builder #2 is helpful for building up a value from data that could fail, like a JSON decoder or validator.

Examples:
[https://package.elm-lang.org/packages/stoeffel/elm-verify/latest/](https://package.elm-lang.org/packages/stoeffel/elm-verify/latest/)
[https://package.elm-lang.org/packages/NoRedInk/elm-json-decode-pipeline/latest](https://package.elm-lang.org/packages/NoRedInk/elm-json-decode-pipeline/latest)

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1487813359177240576) as part of [Ship 30 for 30](https://www.ship30for30.com/).