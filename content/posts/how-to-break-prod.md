---
title: "How to break prod"
description: ""
tags: [ software, teams ]

date: 2022-01-19T16:26:41.000Z
---

Yesterday my coworker's PR caused a site outage for 10 minutes.

Taking down production is nobody's idea of a good time!

But the way they handled it was so exemplary that they got praise from our manager.

Here's what they did:

🙋 Responded to reports with relevant work

When they saw bug reports come in and made the connection, they pointed out their PR as a possible cause:

"This might be because of my PR: [GitHub link]"

⏪ Reverted the change as quickly as possible

They re-ran the last successful build, so that the site would be back up ASAP.

Then they opened a PR to revert the change in master.

📣 Let the full team know

They announced the issue to all staff, including:

⏱ When the outage began
👀 How it would be reported by a customer
🆗 The current status of the issue

🔍 Identified the cause

As they confirmed that the site was back up, they began analyzing the issue.

They reported their debugging process in a Slack channel, public to the rest of the dev team.

🔧 Removed the cause of the issue

Not only did they fix this instance of the problem—they also put a fix in place that would prevent this type of issue from happening again.

📣 Announced when the issue was resolved

Updated the full team—including:
✅ The issue was resolved
💫 The cause was identified and is no longer possible
🙏 Apology for any inconvenience
👂 They were available for any questions

My coworker's instincts were excellent, but we can all act this way if we're prepared!

You can support your team's quick action in crisis response by having a playbook with steps like the ones in this thread—and by making each technical step as easy to take as it can be.

---

This post was originally a [Twitter thread](https://twitter.com/DuncanMalashock/status/1483838332392120321) as part of [Ship 30 for 30](https://www.ship30for30.com/).