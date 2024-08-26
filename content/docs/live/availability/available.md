---
weight: 1
draft: false
toc: false
title: "Available Assets"
description: "API to list all the current available assets"
---

Obtain a list of all currently available assets, containing the most important data common to all of them.
All the response fields specified in the table below are mandatory.

HTTP Request:
```
GET /available/all
```

<br>

Example of successful response:
```json
{
  "success": true,
  "data": {
    "count": 2,
    "list": [
      {
        "code": "USD",
        "name": "Dollar",
        "decimalPlaces": 2,
        "symbol": "$",
        "type": "currency"
      },
      {
        "code": "BTC",
        "name": "Bitcoin",
        "decimalPlaces": 8,
        "symbol": "₿",
        "type": "crypto"
      }
    ]
  }
}
```

{{< table "table-striped table-responsive" >}}
|      Field                        |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "success"                         | Boolean                | HTTP Request is successful, if it's false you have to [handle the error](/docs/quickstart/errors/) |
| "data"                            | Object                 ||
| "data", "count"                   | Integer                | Length of the result list |
| "data", "list"                    | Array                  | Result list |
| "data", "list", \<element\>, "code" | String               | Listing code of the asset |
| "data", "list", \<element\>, "name" | String               | Name of the asset |
| "data", "list", \<element\>, "decimalPlaces" | Integer     | Minimum subunit of the asset |
| "data", "list", \<element\>, "symbol" | String             | Graphic symbol of the asset |
| "data", "list", \<element\>, "type" | String enum          | Kind of asset, can be `currency`, `crypto`, `material` |
{{< /table >}}
