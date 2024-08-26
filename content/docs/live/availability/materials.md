---
weight: 4
draft: false
toc: false
title: "Available Materials"
description: "API to list all the current available materials"
---

Obtain a list of all currently available materials.
The response shows only materials (e.g. Gold) and contains all the data available in
[assets endpoint](/docs/live/availability/available/), plus some specific data available only for materials.

HTTP Request:
```
GET /available/materials
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
        "code": "XAG",
        "name": "Silver Ounce",
        "decimalPlaces": 2,
        "symbol": "Ag",
        "ounces": "1",
        "grams": "28.349523125"
      },
      {
        "code": "XAU",
        "name": "Gold Ounce",
        "decimalPlaces": 2,
        "symbol": "Au",
        "ounces": "1",
        "grams": "28.349523125"
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
| "data", "list", \<element\>, "code" | String               | Listing code of the material |
| "data", "list", \<element\>, "name" | String               | Name of the material |
| "data", "list", \<element\>, "decimalPlaces" | Integer     | Minimum subunit of the material |
| "data", "list", \<element\>, "symbol" | String             | Graphic symbol of the material |
| "data", "list", \<element\>, "ounces" | Decimal string     | Weight in ounces of the material |
| "data", "list", \<element\>, "grams"  | Decimal string     | Weight in grams of the material |
{{< /table >}}

<br>

> ⚠️ The decimal values are passed as strings to avoid loss of precision during the data transfer and JSON decode.
> You could parse them into a floating point value, but we advise you to use something like BigInteger.