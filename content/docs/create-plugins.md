+++
title = "How to Create Plugins"
description = "Developer guide for creating JakeyTTS plugins."
weight = 100
+++

The updated JakeyTTS WebSocket API allows remote subsystems to inject dynamic global variable tokens, establish customized signal modulators, register slash macros, and push telemetry frames back into the central framework workspace seamlessly.

## 1. Infrastructure Server Connection & Process Routing
The central asynchronous core initializes an automated local loopback pipeline engine instance monitoring network connection threads on `ws://localhost:8889/`.

**Automated Execution Lifecycle Engine Specification**
To eliminate manuals user configuration dependencies entirely, developers transmit runtime properties dynamically inside the registration handshake package. The server automatically routes process management requests based on the criteria below:
- `decoupled_client` (Listen Only): Triggered when executable parameters are omitted. The framework registers the module properties but leaves application loop lifecycles unmanaged.
- `managed_process` (Auto Spawn/Kill): Triggered when path parameters are present. The framework maps file strings to local execution bins, automatically booting up modules upon approval.

## 2. Registration Handshake Manifesto
Immediately following network socket connection, sub-processes must dispatch a registration payload detailing scopes, icon descriptors, binary execution paths, and metadata signatures:

```json
{
  "type": "register",
  "payload": {
    "id": "diapstash-automation-plugin",
    "name": "DiapStash Integration Bridge",
    "version": "1.0.0",
    "protocol_version": "1.0",
    "icon": "iVBORw0KGgoAAAANSUhEUgAA...",
    "executable_path": "C:\\Plugins\\DiapStash\\bridge.exe",
    "launch_invisible": true,
    "subscriptions": ["redeems", "commands"]
  }
}
```

## 3. Core TTS Loop Interactions
To enqueue asynchronous audio rendering assignments directly onto the server generation channels, execute a `speak_request` packet command:

```json
{
  "type": "speak_request",
  "payload": {
    "text": "Speech pipeline automated transmission message."
  }
}
```

## 4. Programmatic Global Variables System
External sub-processes can push native decoupled key-value tokens into the memory workspace pool. Once injected, users can embed these entities anywhere inside chat templates or custom redeems layouts using the dynamic brace syntax schema `{variable_name}`:

```json
{
  "type": "set_global_variable",
  "payload": {
    "variable_name": "diapstash_product",
    "variable_value": "SUNKISS Masterpiece (Blue)"
  }
}
```

## 5. Capability Hook Injections & DSP Modulators
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
