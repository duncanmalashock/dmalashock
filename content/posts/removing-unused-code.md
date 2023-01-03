---
title: "Removing unused code automatically"
description: ""
tags: [ elm, software ]

date: 2022-01-11T16:40:08.000Z
---

Every Monday, I approve and merge an auto-generated PR that removes all unused code in our 223k LOC front-end application.

If you use [Elm](https://twitter.com/elmlang), you can do this too! Here's how:

### 📂 Install and init `elm-review` in your project

elm-review ([https://github.com/jfmengels/elm-review](https://github.com/jfmengels/elm-review)) by [Jeroen Engels](https://twitter.com/jfmengels) is a static analysis tool.

It allows you to define rules to apply to your source code, and tells you which parts don't follow them.

It can also fix problems automatically!

### ⚙️ Set up an `elm-review` config

In the new `review` folder, set up your `ReviewConfig.elm` file.

Here's an example that removes all unused functions and types except for those in the `DontScanMe` directory:

[https://gist.github.com/duncanmalashock/70a9eef633523423fe57cf55e3ebce12](https://gist.github.com/duncanmalashock/70a9eef633523423fe57cf55e3ebce12)

Run `npx elm-review` to make sure it works!

### 📄 Create a YAML configuration for a GitHub Action

Using GitHub Actions allows PRs to be created automatically on a schedule.

Here's an example config:

[https://gist.github.com/duncanmalashock/8d92c2e618abd606e14b51a24cbdbd19](https://gist.github.com/duncanmalashock/8d92c2e618abd606e14b51a24cbdbd19)

### ⬆️ Commit your changes and push to GitHub

That's it! At the time you specified in the YAML file, you'll see a PR that removes your project's unused code.

Thanks to [Jeroen Engels](https://twitter.com/jfmengels) for `elm-review`, a great tool for maintaining your codebase! ❤️

---

<small>This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1480942614966845443) as part of [Ship 30 for 30](https://www.ship30for30.com/).</small>