+++
title = "3. Core TTS Loop Interactions"
description = "Core TTS Loop Interactions"
weight = 30
icon = "spatial_audio_off"
+++

To enqueue asynchronous audio rendering assignments directly onto the server generation channels, execute a `speak_request` packet command:

```json
{
  "type": "speak_request",
  "payload": {
    "text": "Speech pipeline automated transmission message."
  }
}
```
