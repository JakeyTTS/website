---
title: "JakeyTTS 2.0.2 Quick Fix: Twitch Redeem Reply Fixed"
date: 2026-05-31T20:00:00+02:00
draft: false
description: "A quick hotfix (v2.0.2) has been released to address an issue where Twitch redeem reply messages were not appearing in chat."
type: "blog"
layout: "single"
author: "abdldavid"
image: "images/blog/jakeytts_banner.png"
tags: ["release", "hotfix", "twitch", "bugfix"]
---

Hello everyone,

I'm pushing out a quick hotfix today with **JakeyTTS 2.0.2**. 

Following the 2.0.1 release, some of you noticed that Twitch channel point redeems were executing the Text-to-Speech audio successfully, but the automated reply message in chat was failing to send. This has now been fully resolved!

---

# What Was Fixed?

* **Twitch Redeem Chat Replies**: Fixed a bug in the Twitch integration client where automated chat replies associated with custom channel rewards/redeems were not being sent to the Twitch chat room.

If you have custom messages configured to send in chat when a viewer redeems a reward (for example, confirming that their TTS request has been queued), these will now correctly post to chat again.

---

# How to Update

Since this is a quick hotfix, the update process is extremely simple:

1. **[Download JakeyTTS v2.0.2](https://github.com/JakeyTTS/JakeyTTS/releases/download/v2.0.2/JakeyTTS_v2.0.2.exe)** (Direct `.exe` installer).
2. Run the installer to overwrite your current installation. All your existing settings, voice configurations, and custom melodies will be safely preserved.

> [!IMPORTANT]
> Make sure to close your active JakeyTTS application before running the installer to prevent file lock errors.

---

# Supporting the Project

As a reminder, JakeyTTS is entirely free and open-source. Since my health limits my ability to seek standard employment and I am trying to fund a new powered wheelchair, your support on Ko-fi means the world to me.

* **Support my Powered Wheelchair Fund:** **[ko-fi.com/abdldavid](https://ko-fi.com/abdldavid)**

Thank you all for reporting the issue so quickly! If you find any other bugs or have feedback, please reach out in the official Discord server.

Happy streaming!  
**David (abdldavid)**
