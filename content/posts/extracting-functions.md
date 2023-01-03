---
title: "Extracting a function: why and when?"
description: ""
tags: [ elm, software ]

date: 2022-02-03T13:33:11.000Z
---

Extracting a function may be simple, but it's a great tool for clarifying your code.

But when should you do it, and when should you avoid it?

Here are a few thoughts:

There are 3 benefits to extracting a function:

1️⃣ It summarizes code
2️⃣ It allows for reuse
3️⃣ It enables consistency

And there is 1 drawback:

⛔️ It hides detail

Let's go into each of these one by one.

1️⃣ It summarizes code

By extracting a function, your function calls read as high-level summaries of what the code does.

This gives you opportunities to break your problems down into steps, and allow your solution to be read that way by others.

2️⃣ It allows for reuse

An obvious benefit of an extracted function is that you'll be able to call it in other places.

If your code needs to be used in two places, this benefit usually outweighs any drawbacks.

3️⃣ It enables consistency

Subtly different from 2️⃣, an extracted function means changes to the function affect every usage in the same way.

If you copy-and-paste instead of extracting, you are setting yourself up for mistakes when one instance changes and another doesn't.

⛔️ It hides detail

The drawback is that an extracted function moves the details of the code to another place (the function definition).

This can break the flow of reading if you 're looking for a specific detail or following a chain of function calls.

So extract a function if:

✅ You're reusing code, or
✅ Your code would be more easily skimmed

But avoid it if not.

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1489230486186737668) as part of [Ship 30 for 30](https://www.ship30for30.com/).