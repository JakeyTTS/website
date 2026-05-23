+++
title = "2. Registration Handshake"
description = "Registration Handshake Manifesto"
weight = 20
icon = "handshake"
+++

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

### Upgraded Handshake Field Payload Specifications

| JSON Parameter | Data Type | Handshake Parameter Requirement Specification |
| :--- | :--- | :--- |
| `type` | `string` | Must equal `'register'` precisely to initialize authentication validation layouts. |
| `payload.id` | `string` | The absolute system unique layout string identifier for your extension (e.g., `'discord-voice-bridge'`). |
| `payload.icon` | `string (Base64)` | Raw customized graphics asset file encoded as a continuous base64 text stream. Renders directly as the tile avatar container on the extension page workspace grid. |
| `payload.executable_path` | `string (Path)` | The path targeting local execution bin files. If provided, the central framework takes control of process initialization states automatically. Omit to run as decoupled clients. |
| `payload.launch_invisible` | `boolean` | When true, shifts background compilation process threads inside isolated CreateNoWindow states when launched by the user. |
| `payload.subscriptions` | `array [string]` | Array string targets specifying desired hooks to intercept telemetry channels. Supported: `'chat'`, `'commands'`, `'redeems'`, `'bits'`, `'subs'`, `'test'`. |
