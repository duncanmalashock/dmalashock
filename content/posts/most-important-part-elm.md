---
title: "The most important part of writing Elm"
description: ""
tags: [ elm, software ]

date: 2022-01-21T14:24:28.000Z
---

In [Elm](https://twitter.com/elmlang), modeling data accurately is more valuable than writing good algorithms.

With clear data modeling, errors that are possible in your program will be fewer, and your codebase more coherent. But doing it well can be a hard skill to develop!

Try to form these habits:

### ✅ Use custom types for conditional data

Some data is only present in a particular case.

If our type is `Animal`, a `Fish` has no `Feathers`, and a `Bird` has no `Scales`. These constraints are possible in Elm!

Use custom types to include conditional data only when needed.

### 🤷 Use `Maybe` as rarely as possible

Since all cases must be handled explicitly, `Maybe`s can multiply the conditions to handle and make your code hard to work with.

When nullable data starts accumulating, consider a custom type to create guarantees.

### 🤔 Reconsider primitive types

You may be used to using `Bool`s and `String`s in other languages.

But sometimes `String`s don't constrain possible values enough.

`Bool`s are not descriptive, and they won't allow for the addition of further options if they come up.

### ❓ Use type variables as a last resort

Type variables can be helpful abstraction tools. But does your custom type really need to allow for any possible type to be used?

Try starting from a more constrained set first, and use a type variable only if it's necessary.

### 🤹 Try different approaches

Given a domain concept, how many ways could you model it, and with what other data types?

In Elm, refactoring is aided by the compiler! Change your model, and see how different attempts can make your code easier or harder to work with.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1484532350226780163) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>