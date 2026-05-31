---
title: "JakeyTTS 2.0 is Officially Available!"
date: 2026-05-28T20:00:00+02:00
draft: false
description: "JakeyTTS 2.0 is officially released! Read about the journey of evolving from a simple script into a native Windows 11 desktop app, explore its key features, and find out how you can support my powered wheelchair fund."
type: "blog"
layout: "single"
author: "abdldavid"
image: "images/blog/launch/jakeytts_launch_banner.png"
tags: ["release", "announcement", "jakeytts", "kofi", "winui3"]
---

Hello everyone,

It's official: **JakeyTTS 2.0 is finally here!** After an intense, passionate month of development, the client is ready for public release. What started as a simple, custom tool to help my friend Jakey with his streams has now evolved into a fully realized desktop application.

I'm incredibly proud of how far this project has come, and I can't wait for you all to try it out.

---

# The Evolution: From a Script to a Native Windows 11 App

Just one month ago, JakeyTTS was a small, experimental script with a rudimentary layout. I wanted to build something lightweight that could run locally, integrate with Twitch, and bypass the limitations of generic, cloud-based web synthesizers. 

Here are some of the earliest designs when I first started hacking the interface together in Visual Studio:

| Early Layout Concept | Initial VS Interface |
| :---: | :---: |
| ![Early GUI Design](/images/blog/launch/jakeytts_first_version.png) | ![Visual Studio Early Prototype](/images/blog/launch/first_version_ide.png) |
| *One of the very first GUI drafts for the client.* | *The early prototype layout running inside the IDE.* |

During the past month, those simple windows and basic elements underwent a complete ground-up rewrite. By leveraging **WinUI 3** and modern design principles, JakeyTTS has transformed into a  native Windows 11 desktop application. It integrates with the modern Windows design system, featuring fluid animations, dark mode, and a highly responsive, clean user experience.

![Modern JakeyTTS Dashboard](/images/home_jakeytts.png)
*(The modern, polished JakeyTTS 2.0 homepage dashboard)*

---

# What is JakeyTTS? A Quick Overview

For those new to the project, **JakeyTTS** is a free, lightweight, and local Text-to-Speech client built specifically for streamers, content creators, and their communities. Because everything runs locally on your PC, you don't need active cloud subscriptions or external APIs to generate high-quality speech.

Here are the key features that make JakeyTTS 2.0 stand out:

*   **Native Twitch Integration**: Connect your channel in seconds to let your viewers trigger TTS commands, channel point rewards, and sound cues directly from chat.
*   **Custom Mixed Voices**: Create unique hybrid voice profiles. You can blend up to 10 different voice models across multiple languages (e.g., American English, British English, Spanish, Japanese) with a visual, self-normalizing weight system.
*   **Melody Graph Editor**: Let your viewers "sing"! Define musical pitch curves using our visual node editor to recreate vintage, synth-like vocal melodies (inspired by *Tomodachi Life*).
*   **Audio Tag Modifiers**: Tweak vocal output dynamically using inline chat tags like `[robot]`, `[reverse]`, `[echo]`, `[speed:X]`, and `[pitch:Y]`.
*   **Pronunciation Dictionary**: Teach the engine how to pronounce complex usernames, internet slang, or acronyms so your stream alerts always sound natural.
*   **Plugin Architecture**: Extend the app's capability with external integrations, such as the recently launched **DiapStash Stream Automation Hub**.

---

# Supporting the Project & My Wheelchair Fund

This project is open-source and free to download. For me, developing JakeyTTS has been an intense but rewarding journey and a way to give back to a community that has made me feel welcome and valued.

As many of you know, I live with a neuromuscular disease that severely limits my mobility and causes significant fatigue. To navigate the outside world and perform daily tasks, I rely on a **powered wheelchair**. 

Because of my physical limitations, standard employment isn't feasible, and my development setup is currently running on a 10-year-old PC that struggles with modern IDEs. 

To help support the ongoing development of JakeyTTS and help me fund my mobility needs, I have set up a Ko-fi page:

> [!IMPORTANT]
> **Support me on Ko-fi:** **[ko-fi.com/abdldavid](https://ko-fi.com/abdldavid)**  
> *All donations and funding from this page will go directly towards my powered wheelchair fund. The current WheelChair is no longer suitable for my needs and repairing it would cost me the same as buying a new one.*

Any contribution, no matter how small, makes an immense difference in my quality of life and allows me to keep coding and improving these tools.

---

# Get Started with JakeyTTS 2.0

JakeyTTS 2.0 is extremely lightweight, requiring less than 700 MB of disk space and minimal background CPU usage.

1.  **[Download JakeyTTS 2.0](https://github.com/JakeyTTS/JakeyTTS/releases/download/v2.0.2/JakeyTTS_v2.0.2.exe)** (Direct `.exe` download).
2.  Follow the **[Installation Guide](/docs/install/)** to set up your environment (.NET 8.0 Runtime required).
3.  Read the **[Twitch Integration Docs](/docs/configure-tts/)** to connect your channel.

Thank you so much to everyone in the Jakey Streams, and the community who helped test the early versions, gave feedback, and shared this journey with me. Your encouragement keeps me going every day! 🥹

With gratitude,  
**David (abdldavid)**
