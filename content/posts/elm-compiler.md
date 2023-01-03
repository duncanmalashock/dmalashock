---
title: "What I learned from the Elm compiler"
description: ""
tags: [ elm, software ]

date: 2022-02-02T14:49:59.000Z
---

Yesterday my teammate [Matthew Griffith](https://twitter.com/mech_elephant) and I spent some time reading the source code of the [Elm](https://twitter.com/elmlang) compiler together.

I don't know much about compiler design (or Haskell). So this was a fun learning experience!

Here's what I learned about the general phases of compilation:

1️⃣ Scanning

Compilers start by reading source code and scanning it into a series of "tokens".

Tokens are the "parts of speech" of a language like:
- numbers: 0, 3.14...
- symbols: {, }, =, (, )...
- identifiers: myVariable, myType...
- reserved words: type, module...

2️⃣ Parsing

A compiler parses this list of tokens into a tree structure called a syntax tree, that reflects the structure of the language.

If the tree can't be formed correctly, this is the point where a compiler would report syntax errors.

3️⃣ Static analysis

Having parsed the source code into a tree, this is the point where a compiler attempts to "resolve" all of its "identifiers".

"Resolution" is answering questions like "Where is myVariable defined?"

This phase is also when type checking is done.

4️⃣ Intermediate representation

Compilers may transform the resolved and type-checked tree into a form that is more agnostic of the source code or any particular build target.

This can prepare for optimization and code generation for multiple possible platforms.

5️⃣ Optimization

The compiler attempts to improve the performance of the code to be generated.

This could include:
- Simplifying expressions if they are constant
- Minifying identifier names
- Removing unused code

6️⃣ Code generation

At this stage the compiler uses its optimized tree to generate the build target, resulting in an executable program.

☝️ Fun fact

One thing I learned about Elm is that it doesn't do "dead code elimination".

Because it walks the tree from an entry point and follows function calls, unused code is not reachable. So "dead code" is never included in the first place!

Thanks to [Matthew Griffith](https://twitter.com/mech_elephant) for pointing me to this book: [craftinginterpreters.com/contents.html](https://craftinginterpreters.com/contents.html) — take a look if you're curious about compilers.

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1488887428077260803) as part of [Ship 30 for 30](https://www.ship30for30.com/).