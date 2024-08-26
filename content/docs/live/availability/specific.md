---
weight: 2
draft: false
toc: false
title: "Check Asset"
description: "API to check if a specific asset is available"
---

Check if a specific asset is currently available and obtain its details

HTTP Request:
```
GET /available/all/{code}
```

<br>

HTTP Request Example:
```
GET /available/all/EUR
GET /available/all/USD
```

<br>

Common Errors:
- 404, "ASSET_NOT_FOUND"

Example of successful response:
```json
{
  "success": true,
  "lastUpdate": "2024-08-26T13:20:28.292761976Z",
  "data": {
    "code": "EUR",
    "name": "Euro",
    "decimalPlaces": 2,
    "symbol": "€",
    "type": "currency"
  }
}
```

{{< table "table-striped table-responsive" >}}
|      Field              |   Type                 |  Description |
|:-----------------------:|:----------------------:|:-------------|
| "success"               | Boolean                | HTTP Request is successful, if it's false you have to [handle the error](/docs/quickstart/errors/) |
| "data"                  | Object                 ||
| "data", "code"          | String                 | Listing code of the asset |
| "data", "name"          | String                 | Name of the asset |
| "data", "decimalPlaces" | Integer                | Minimum sub-unit of the asset |
| "data", "symbol"        | String                 | Graphic symbol of the asset |
| "data", "type"          | String enum            | Kind of asset, can be `currency`, `crypto`, `material` |
{{< /table >}}
