---
title: "UI design patterns in Elm"
description: ""
tags: [ elm, software ]

date: 2022-01-28T18:23:23.000Z
---

In [Elm](https://twitter.com/elmlang), your UI elements don't need to be "components" the way they might be in React.

So what should they be? Here are a number of common patterns for different requirements:

1️⃣ Simple parameters

`view : String -> (String -> msg) -> Html msg`

Use this when view code varies in few ways, and all parameters are required.

2️⃣ Config parameter

`view : Config msg -> Html msg`

Create a `Config` type and use this pattern when some parameters are optional, or could benefit from sensible defaults.

More about the Config pattern:
[https://sporto.github.io/elm-patterns/basic/builder-pattern.html](https://sporto.github.io/elm-patterns/basic/builder-pattern.html)

3️⃣ Model, Msg, update

`view : Model -> Html Msg`
`update : Msg -> Model -> (Model, Cmd Msg)`

Create a `Msg` type and use this pattern when there are too many parameters (data and `msg`s) to pass in.

4️⃣ Returning ParentMsg

`view : Model -> Html Msg`
`update : Msg -> Model -> (Model, Cmd Msg, Maybe ParentMsg)`

Use this pattern when a view needs to send data to an `update` function above it in the hierarchy.

☝️ Use the simplest pattern you can

It can be tempting to treat your view code as uniform "components".

But there's no need to use 4️⃣ for everything—in many cases it would be too much work!

Remember: there is no such thing as "parent-child communication" with pure functions.

Thanks to [Richard Feldman](https://twitter.com/rtfeldman) for his explanation of these concepts in his talk "Scaling Elm Apps":
[https://www.youtube.com/watch?v=DoA4Txr4GUs](https://www.youtube.com/watch?v=DoA4Txr4GUs)

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1487129193326465028) as part of [Ship 30 for 30](https://www.ship30for30.com/).