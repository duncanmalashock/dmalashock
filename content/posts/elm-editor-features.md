---
title: "The Elm editor features I love"
description: ""
tags: [ elm, software ]

date: 2022-01-20T14:43:40.000Z
---

I switched to an editor I don't like (WebStorm) for [Elm](https://twitter.com/elmlang) development—and I'm happy about it.

I much prefer VS Code's UX. But [Keith Lazuka](https://twitter.com/klazuka)'s plugin for IntelliJ editors ([https://github.com/klazuka/intellij-elm](https://github.com/klazuka/intellij-elm)) can do too many amazing things.

Here are some of the features that made me switch:

### 🕵️ Find all usages

Highlight a type or function, and the editor will find all usages of it throughout your codebase.

It uses the AST, so it's type-aware—much more effective than text-based search.

### ✍️ Rename all instances

Similarly, the type-aware find-and-replace applies to all usages and all type annotations.

Changing names is as easy as it can be—rename any of your functions, types, and type variants.

### 🗑 Detect unused code

Because of Elm's language design, it's easy to tell via static analysis whether code is ever used.

Unused imports, function, types, and variants show up in gray in your editor—no need to even run a command to find them!

### 🗃 Auto-import / Auto expose

If you need a function, just use it—the editor will give you the option to add an import without scrolling to the top of your file.

It can also expose/un-expose code defined in your module.

### 🪄 Code generation

One of my favorite features allows you to generate the boilerplate for destructuring a type.

Just run the command and it creates all the branches you need.

It can also generate JSON decoders for a given type!

Want to make your Elm experience a breeze? Give it a try: [https://github.com/klazuka/intellij-elm](https://github.com/klazuka/intellij-elm)

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1484174797311512576) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>