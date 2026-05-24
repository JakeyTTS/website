+++
title = "6. Remote Web UI Ingestion"
description = "Embed administrative panels or dashboards natively within the JakeyTTS workspace."
weight = 60
icon = "web"
+++

Embed administrative panels or dashboards natively within the central NavigationView framework window workspace:

```json
{
  "type": "inject_ui_page",
  "payload": {
    "embed_url": "https://api.diapstash.com/api/docs/"
  }
}
```

## UI Injection Parameter Specifications

| JSON Key | Type | Rendering Layout Requirement Rules |
| :--- | :--- | :--- |
| `type` | `string` | Must equal `'inject_ui_page'` to trigger dynamic menu tab insertions. |
| `payload.embed_url` | `string (URL)` | The target URL page. Pushes an adaptive container inside navigation boundaries executing integrated WebView2 web runtimes. |
