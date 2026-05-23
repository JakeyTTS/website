+++
title = "Introduction"
description = "Overview of the JakeyTTS chat commands and variable system."
icon = "info"
weight = 5
+++

JakeyTTS provides a highly customizable chat commands system, enabling streamers to build interactive, dynamic, and conditional responses for their viewers.

## Command Systems

The JakeyTTS command engine is split into two configurations depending on your complexity needs:

### 1. Standard Commands
Standard commands let you quickly map chat triggers (e.g. `!hello`) to speech, chat responses, or plugin actions. You can also define custom **Variables**—including **Scalars** (text or numbers) and **Lists** (for random pools like jokes or quotes)—and reference them dynamically within your messages.

For setup details, see the [Standard Commands & Variables](standard/) guide.

### 2. Advanced Action Blocks
Action Blocks upgrade your command logic into sequential, step-by-step scripts. You can chain actions, inject delays (in milliseconds), roll randomizer numbers, evaluate complex conditional rules (`If Condition`), and update global or local variables on the fly.

For setup details, see the [Advanced Action Blocks](blocks/) guide.
