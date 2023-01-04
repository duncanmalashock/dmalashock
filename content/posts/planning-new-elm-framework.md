---
title: "Planning a new Elm application framework with Ryan Haskell-Glatz"
description: ""
tags: [ elm, software ]

date: 2022-05-07T11:51:24.000Z
---

I had a blast helping [@rhg_dev](https://twitter.com/rhg_dev) get started on his new [Elm](https://twitter.com/elmlang) app framework!

Here are a few topics we covered:

### 1️⃣ Defining the audience

Ryan wanted the docs to be great, but he needed more clarity on how to make that happen.

To get more focus, we explored a few questions:

- 🤷 Who are we talking to?
- 🤕 What is their problem?
- 🧠 What do they know already?

After exploring a number of different potential audiences, we chose two that seemed like they'd be best served by Ryan's project:

1. 👀 JS devs who want to easily evaluate Elm as an option
1. 🌳 Elm devs who want a simple, reliable app architecture

### 2️⃣ Reviewing comparable frameworks

Ryan wants devs who try Elm to have easy, familiar experiences that feel like the quick-start guides that popular frameworks have.

To do that, we looked to the JS community, to learn from the guides for these other frameworks.

Along with getting ideas for helpful guide content, we found some inspirations for features that an `init` command might do:

- 🙋 Prompt the user for their project name and what to include
- 🪄 List what files and folders were created
- 💁 Provide next commands a user might run

### 3️⃣ "Guide-Driven Development"

Ryan didn't want to get ahead of himself when it came to feature development.

And he also wanted high-quality guides that wouldn't break when features changed.

So we tried a TDD approach, where guide content would be used as the test input.

In about an hour of "guide-driven" testing and development, Ryan had a working `init` command, that:

- 🪄 Lists the files it created
- 🔒 Is guaranteed to match the input and output in the guide

I had a lot of fun, and I'm looking forward to what Ryan comes up with next!

You can watch our pairing session on Twitch (VODs are online for two weeks), and check out his other streams at [twitch.tv/ryan_the_nerd](https://www.twitch.tv/ryan_the_nerd)

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1522906945530826752).</small>