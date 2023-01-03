---
title: "How to choose better names"
description: ""
tags: [ software, names ]

date: 2022-01-17T14:29:20.000Z
---

Have you ever said "naming things is hard!", but didn't know what to do about it?

I've been reading [Felienne Hermans](https://twitter.com/Felienne)'s book and I've learned that improving names in your codebase may be more straightforward than you think!

Here are a few things about names in code that surprised me:

😓 Why is naming hard?

Naming happens while solving problems, when we are using our brains the most and have little mental energy to spare.

And name choice isn't consistent—in studies, two programmers only chose the same name for a variable or method 7% of the time.

🤷 Why name things well?

Names make up the majority of code—72% of a large typical codebase.

Naming issues come up often—they were found in 25% of code reviews studied.

Names affect debugging—in studies, developers could find 19% more bugs when reading code with good names.

🐛 Code with bad names has more bugs

Research has found a statistically significant correlation between bug frequency and bad names.

"Bad names" includes names with syntactic issues, and ones that use non-dictionary words.

⚙️ How good names work

Good names support "chunking", a compression method aided by the short-term memory.

Clear names with well-chosen words help the long-term memory make connections to a problem domain.

Names with consistent syntactical formats are easier to process.

🍱 Patterns for naming

Programmers use "name molds"—templates that words fit into.

Here is the same naming idea, with different molds used: `maxX`, `maxXPerY`, `maxNumberOfX`, `maxXAmount`, "yXLimit`

Keeping molds consistent in code helps the long-term memory.

📚 Word choice

Using dictionary words vs. letters or abbreviations makes names easier to understand.

Using consistent words for the same idea helps the long-term memory.

Using multiple words for the same idea creates ambiguity (e.g. "are these the same, or subtly different?")

💫 How can we choose better names?

Review names after code has been written, when you have more mental space.

Keep a "project lexicon" to helpfully constrain word options for consistency.

Review the name molds your project uses and choose ones to adhere to intentionally.

🛠 How can tools help us?

When I read these ideas, I thought of static analysis tools like [Jeroen Engels](https://twitter.com/jfmengels)'s `elm-review`.

Given a project lexicon and a list of name molds, could a rule be written to evaluate whether new names used in a PR were consistent, and suggest improvements?

📖 Curious to learn more?

Read "The Programmer's Brain" by Felienne Hermans: [https://www.manning.com/books/the-programmers-brain](https://www.manning.com/books/the-programmers-brain)

Check out `elm-review` by Jeroen Engels: [https://github.com/jfmengels/elm-review](https://github.com/jfmengels/elm-review)

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1483084025224966149) as part of [Ship 30 for 30](https://www.ship30for30.com/).