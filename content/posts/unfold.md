---
title: "The opposite of `fold`"
description: ""
tags: [ elm, software ]

date: 2022-01-29T16:36:08.000Z
---

If you write [Elm](https://twitter.com/elmlang), you may have worked with fold functions like `List.foldl`.

Yesterday I chatted with [Joël Quenneville](https://twitter.com/joelquen) and learned about `unfold`, a kind of inverse process, and how it can be useful.

Here's my summary:

Where `fold` takes:
- A reducing function
- An initial data type (e.g. `Tree`, `List`)
- A list

And returns:
- A new data type with all the list values reduced into it.

`foldl : (a -> b -> b) -> b -> List a -> b`

`unfold` does the opposite.

It takes:
- A function for generating new values
- An initial data type (e.g. `Tree`, `List`)

And returns:
- A list of values

`unfold : (a -> Maybe (b, a)) -> a -> List b`

This can be used for generating a list of values from a data source.

Here's an implementation of `unfold`, and a sample program that generates a range of integers:
[ellie-app.com/gxGHDzCYp5va1](https://ellie-app.com/gxGHDzCYp5va1)

For you FP jargon-heads out there, I learned an unfold is called an "anamorphism".

I won't be saying that too much, but do what you will with that knowledge: [https://en.wikipedia.org/wiki/Anamorphism](https://en.wikipedia.org/wiki/Anamorphism)

Thanks to [Joël Quenneville](https://twitter.com/joelquen) for the clear explanations, as ever!

Curious to learn more? 

Watch Joël's talk: "Inverting a Binary Tree with 1 Line of Elm" at the Elm Online Meetup:
[https://www.youtube.com/watch?v=dSMB3rsufC8](https://www.youtube.com/watch?v=dSMB3rsufC8)

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1487464589671477251) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>