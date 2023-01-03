---
title: "Functional programmers don't need to know category theory"
description: ""
tags: [ elm, software ]

date: 2022-01-31T14:31:49.000Z
---

Functional programmers don't need to know terms from category theory.

Understanding terms like "functor", "applicative", and "monad" doesn't help you solve problems.

What does help is understanding the functions they involve.

Here's what I mean 👇

Let's say you're implementing a type:

`type MyType a`

There are any number of functions you could implement for working with `MyType`.

Here are a few you might consider:

## 1️⃣ map

`map : (a -> b) -> MyType a -> MyType b`

`map` applies a function to a type's parameter.

Examples:

- `[Maybe.map](http://Maybe.map)` applies a function to `Just` values of a `Maybe`
- `[Html.map](http://Html.map)` lets you transform the `msg` type produced by `Html msg`

### 🤔 When to write `map`?

Will `MyType` be parameterized with types that commonly need functions applied to them, like `msg`?

If so, consider writing `[MyType.map](http://MyType.map)`.

## 2️⃣ andMap

`andMap : MyType a -> MyType (a -> b) -> MyType b`

`andMap` allows a type variable to be a function whose arguments are partially applied.

Example:

- `Json.Decode.Pipeline.required` lets you define fields to be decoded, one by one, via pipeline application.

### 🤔 When to write `andMap`?

Will `MyType`'s type parameter need to be constructed piece-by-piece using partial application?

For instance, is `MyType` is meant to be used for data validation or decoding?

If so, consider writing `MyType.andMap`.

## 3️⃣ `andThen`

`andThen : (a -> MyType b) -> MyType a -> MyType b`

`andThen` allows combining values that might or might not be present.

Examples:

- `Maybe.andThen` lets you map and combine `Maybe`s.
- `List.concatMap` lets you map and combine `List`s.

### 🤔 When to write `andThen`?

Does `MyType` have a case where its type parameter is not present?

Will that type parameter's value need to be combined with another?

If so, consider writing `MyType.andThen`.

So, what does this all have to do with "functors", "applicatives", and "monads"?

Why don't we leave that to the mathematicians?

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1488158078595960837) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>