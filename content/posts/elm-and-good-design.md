---
title: "Elm and good design"
description: ""
tags: [ elm, software, design ]

date: 2022-01-15T15:26:32.000Z
---

In his presentation "What is Success?", [Elm](https://twitter.com/elmlang)'s creator [Evan Czaplicki](https://twitter.com/evancz) admires a Braun radio designed by Dieter Rams:

 "I can't make things as cool as that radio..."

Would Dieter Rams agree? In what ways does the Elm language exemplify Rams's iconic 10 principles of good design?

Let's review each principle.

Good design:

- 💥 Is innovative
- 🔨 Makes a product useful
- 🏺 Is aesthetic
- 💡 Makes a product understandable
- 🕶️ Is unobtrusive
- ⚖️ Is honest
- ⛰️ Is long-lasting
- 🔬 Is thorough
- 🌳 Is environmentally friendly
- 📌 Is as little design as possible

### 💥 Innovative

Elm brings pure functional programming to front-end web development. Front-end had never been served by this paradigm before.

### 🔨 Useful

Elm's static types and pure functions create numerous guarantees, making software development predictable and scalable.

### 🏺 Aesthetic

Members of the Elm community are quick to express the emotional satisfaction of refactoring huge parts of their codebase and arriving at a working result.

### 💡 Understandable

Elm is easy to learn, and its lack of side-effects makes application code easier to understand, maintain and debug.

### 🕶️ Unobtrusive

Most Elm developers use `elm-format`, an automatic formatting tool that is standardized and non-configurable by design. So the layout of most Elm code will not surprise you.

### ⚖️ Honest

Elm requires you to handle all cases of your application state. This removes the possibility of runtime errors due to unhandled cases.

### ⛰️ Long-lasting

Some applications are cheaper to rebuild than to refactor. But Elm applications are easy to refactor confidently, which means codebases can remain useful longer.

### 🔬 Thorough

Elm's custom types allow you to model your domain much more precisely and correctly than is capable with JavaScript objects. This allows program states to be more accurate and less capable of producing errors.

### 🌳 Environmentally friendly

Elm's compiled asset sizes are the smallest among React, Vue, and Angular 2. If all web applications used Elm, their download size would be smaller on average by a factor of (at least) 2.5.

### 📌 Minimal

In the Elm core libraries, there is mostly only one way of doing something (e.g. rendering HTML, producing an HTTP request, parsing, etc.). This minimalism means easier communication between developers on a project.

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1482373643674038277) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>