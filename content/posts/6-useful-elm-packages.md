---
title: "6 useful Elm packages for your web app"
description: ""
tags: [ elm, software ]

date: 2022-01-25T15:15:31.000Z
---

Making a web application in [Elm](https://twitter.com/elmlang)?

Here are a few community libraries that are useful in almost any web application project you might be writing:

### π Pipeline JSON decoding

[https://package.elm-lang.org/packages/NoRedInk/elm-json-decode-pipeline/latest](https://package.elm-lang.org/packages/NoRedInk/elm-json-decode-pipeline/latest)

Even if your application uses a GraphQL API, you'll likely need to decode JSON at some point.

NoRedInk's library makes decoders easier to write by taking advantage of pipeline application.

### π Dict with keys of any type

[https://package.elm-lang.org/packages/pzp1997/assoc-list/latest/AssocList](https://package.elm-lang.org/packages/pzp1997/assoc-list/latest/AssocList)

The built-in `Dict` type only supports keys with `comparable` types. This package allows for keys of any type you use or define.

### π½ Set with keys of any type

[https://package.elm-lang.org/packages/erlandsona/assoc-set/latest/](https://package.elm-lang.org/packages/erlandsona/assoc-set/latest/)

Similar to the above, but for `Set`sβgreat if you need unique value constraints and/or combination and intersection features.

### π― Number formatting

[https://package.elm-lang.org/packages/ggb/numeral-elm/latest/](https://package.elm-lang.org/packages/ggb/numeral-elm/latest/)

An advanced number-formatting package with multiple language support. Has the same features as Numeral.js.

### π Date formatting

[https://package.elm-lang.org/packages/ryannhg/date-format/latest](https://package.elm-lang.org/packages/ryannhg/date-format/latest)

A flexible date-formatting package with clearly named functions that make naming options easier to understand. Has the same features as Moment.js.

### π Time distance in words

[https://package.elm-lang.org/packages/gingko/time-distance/latest/Time-Distance](https://package.elm-lang.org/packages/gingko/time-distance/latest/Time-Distance)

An easy-to-use package that provides time distance in words with multiple language support.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1485994751832772620) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>