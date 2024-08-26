---
weight: 3
draft: false
toc: false
title: "Available Currencies"
description: "API to list all the current available currencies"
---

Obtain a list of all currently available currencies.
The response shows only fiat currencies (e.g. USD) and contains all the data available in
[assets endpoint](/docs/live/availability/available/), plus some specific data available only for currencies.

HTTP Request:
```
GET /available/currencies
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
        "code": "USD",
        "name": "Dollar",
        "decimalPlaces": 2,
        "symbol": "$",
        "obsolete": false,
        "countries": ["AS", "EC", "FM", "GU", "MH", "MP", "PR", "PW", "SV", "TC", "TL", "UM", "US", "VG", "VI"]
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
| "data", "list", \<element\>, "code" | String               | Listing code of the currency |
| "data", "list", \<element\>, "name" | String               | Name of the currency |
| "data", "list", \<element\>, "decimalPlaces" | Integer     | Minimum subunit of the currency |
| "data", "list", \<element\>, "symbol" | String             | Graphic symbol of the currency |
| "data", "list", \<element\>, "obsolete" | Boolean          | True if the currency is no longer used or if another currency has replaced it |
| "data", "list", \<element\>, "countries" | String Array    | `ISO3166-2` country code where the currency is officially used |
{{< /table >}}
