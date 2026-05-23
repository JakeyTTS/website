+++
title = "4. Global Variables System"
description = "Programmatic Global Variables System"
weight = 40
icon = "data_object"
+++

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
