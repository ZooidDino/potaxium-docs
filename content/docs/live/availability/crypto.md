---
weight: 4
draft: false
toc: false
title: "Available Cryptocurrencies"
description: "API to list all the current available cryptocurrencies"
---

Obtain a list of all currently available cryptocurrencies.
The response shows only cryptocurrencies (e.g. BTC) and contains all the data available in
[assets endpoint](/docs/live/availability/available/).

HTTP Request:
```
GET /available/crypto
```

<br>

Example of successful response:
```json
{
  "success": true,
  "data": {
    "count": 1,
    "list": [
      {
        "code": "BTC",
        "name": "Bitcoin",
        "decimalPlaces": 8,
        "symbol": "₿"
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
| "data", "list", \<element\>, "code" | String               | Listing code of the cryptocurrency |
| "data", "list", \<element\>, "name" | String               | Name of the cryptocurrency |
| "data", "list", \<element\>, "decimalPlaces" | Integer     | Minimum subunit of the cryptocurrency |
| "data", "list", \<element\>, "symbol" | String             | Graphic symbol of the cryptocurrency |
{{< /table >}}
