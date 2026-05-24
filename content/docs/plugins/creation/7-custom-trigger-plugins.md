+++
title = "7. Custom Trigger Plugins"
description = "Custom Trigger Plugins & Event Relays"
weight = 70
icon = "bolt"
+++

JakeyTTS allows commands and channel point redeems to trigger custom actions on specific plugins. In order for a plugin to receive these event payloads over WebSocket, it must register support during handshake subscriptions and declare its available trigger variables.

## Step 1: Subscribing & Registering Triggers

When your plugin performs the initial Registration Handshake, include the `'commands'` and/or `'redeems'` scope strings inside the `'subscriptions'` array, and list the trigger variable names in the `'triggers'` array:

```json
{
  "type": "register",
  "payload": {
    "id": "diapstash-automation-plugin",
    "subscriptions": ["commands", "redeems"],
    "triggers": ["diapstash_show"]
  }
}
```

## Step 2: Assigning the Trigger in JakeyTTS

Once your plugin registers, its declared triggers (e.g. `'diapstash_show'`) will show up in the `'Trigger Plugin'` ComboBox column in the Commands or Channel Rewards tables in JakeyTTS. The user maps a command or reward directly to your trigger.

## Step 3: Receiving the WebSocket Trigger Payload

When the command or reward redemption is activated, JakeyTTS dispatches a `'trigger_event'` message over WebSocket. It contains the registered trigger name in the `'trigger'` and `'variable'` keys, allowing you to identify it independently of the user's custom command trigger name:

```json
{
  "type": "trigger_event",
  "payload": {
    "source": "command", // "command" or "redeem"
    "name": "!showoverlay", // user's custom trigger trigger
    "trigger": "diapstash_show", // your registered trigger variable
    "variable": "diapstash_show",
    "user": "StreamerName",
    "message": "optional user chat message input"
  }
}
```

## Trigger Event Payload Parameter Specifications

| JSON Key | Type | Trigger Data Rules |
| :--- | :--- | :--- |
| `type` | `string` | Always `'trigger_event'` for WebSocket message routing. |
| `payload.source` | `string` | Either `'command'` or `'redeem'` indicating which feature triggered the event. |
| `payload.name` | `string` | The trigger name configured by the user (e.g. `'!alert'` or the Twitch Reward name). |
| `payload.trigger` | `string` | The specific trigger variable name (e.g. `'diapstash_show'`) registered by the plugin. |
| `payload.variable` | `string` | Same as `payload.trigger`. Provided for legacy key compatibility. |
| `payload.user` | `string` | Username of the user who executed the command or redeemed the reward. |
| `payload.message` | `string` | The extra text arguments or user input message associated with the trigger. |
