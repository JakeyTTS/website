+++
title = "5. Hook Injections & DSP Modulators"
description = "Capability Hook Injections & DSP Modulators"
weight = 50
icon = "graphic_eq"
+++

Plugins can intercept raw voice data buffers by registering DSP tags. Once hooked, the platform routes outgoing PCM byte arrays to the socket before hardware processing:

```json
{
  "type": "inject_tag",
  "payload": {
    "tag_name": "diapstash_change"
  }
}
```

When the pipeline sounds processing triggers, the server dispatches a `process_audio` event. The plugin must immediately respond with an `audio_processed` envelope carrying back post-filtered base64 raw data within a 1500ms timeout threshold window limit.
