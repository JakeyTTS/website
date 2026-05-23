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

### Speak Parameter Specifications

| JSON Key | Type | Specification Description |
| :--- | :--- | :--- |
| `type` | `string` | Must be `'speak_request'` or `'tts_request'` interchangeably to activate text rendering pipeline workflows. |
| `payload.text` | `string` | The raw message text phrase sent to process into synthesized voice data array frames. |
