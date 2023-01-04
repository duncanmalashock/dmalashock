---
title: "Elm in summary: \"Message Naming Conventions\""
description: ""
tags: [ elm, software, names, summary ]

date: 2022-05-15T15:52:29.000Z
---

I recently rewatched [@noahzgordon](https://twitter.com/noahzgordon)'s conference talk on naming conventions in [Elm](https://twitter.com/elmlang).

It's clear, well-reasoned guidance on an evergreen topic, and I think all Elm devs would benefit from hearing it. Here's my summary:

Conventions reduce decision fatigue and promote helpful practices.

Without conventions, Msg names often vary unhelpfully, describing:

- Events that have happened
- Behaviors that should happen
- Data types involved in an event

A convention should be:

#### 💡 Clear
The reader should immediately understand what it means

#### 💁 Easy
Beginning developers should be able to immediately use it

#### 🔧 Useful
It should promote code that is easy to understand and change

Msg names should answer the following questions:

- 1️⃣ What happened?
- 2️⃣ Who did it?
- 3️⃣ Where and how was it done?

### 1️⃣ What happened?

- Some element was CLICKED
- Some element was HOVERED
- An input field was FOCUSED or BLURRED
- A key was PRESSED
- The mouse was MOVED
- Some data was RECEIVED

### 2️⃣ Who did it?

Was the action performed by:

- The USER
- The CLIENT
- The SERVER
- Some specific WORKER
- Some specific SERVICE

### 3️⃣ (Optionally) Where and how was it done?

For example, specify whether the user clicked on:

- A button
- A modal button
- The bottom-left modal button
- The top-right modal button
- The modal close button

### 💡 Start specific, and remove duplication only when it becomees obvious

Noah gives the example of analytics tracking.

Two buttons that perform the same action should still produce different messages to avoid unnecessary refactors when these separate actions are being tracked.

When following this convention, your Msgs will be named like this:

- UserMovedMouse
- UserClickedSignInButton
- ServerRespondedWithAccountData

Thanks [@noahzgordon](https://twitter.com/noahzgordon) for this great talk! If you haven't seen it before or would like to revisit it, it's on YouTube at [https://www.youtube.com/watch?v=w6OVDBqergc](https://www.youtube.com/watch?v=w6OVDBqergc)

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1525866716164767744).</small>