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
