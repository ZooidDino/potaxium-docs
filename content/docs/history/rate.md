---
weight: 1
draft: false
toc: false
title: "Forex (FX) Rates"
description: "API to retrieve the forex conversion rates related to a date in the past"
---

> Available only in plans starting from [MINIMAL](/docs/pricing/)

Obtain a list of all the daily conversion rates of a specified date using `USD` (Dollar) as the default base currency.

In the following example, `1 USD` = `0.895772375876783 EUR`.

HTTP Request:
```
GET /history
```

<br>

{{< table "table-striped table-responsive" >}}
|      Parameter                    |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "date"                            | Date                   | Reference date of the daily conversion rate, using the `YYYY-MM-DD` format |
| "type"                            | String enum            | (Optional) Get only the specified type of assets, can be `currency`, `crypto`, `material` |
| "assets[]"                        | String array           | (Optional) Get only the specified assets listing codes |
{{< /table >}}

> ⚠️ Minimum supported date is 2000-01-01

<br>

HTTP Request Example:
```
GET /history?date=2023-01-09&type=currency&assets[]=USD&assets[]=EUR
```

<br>

Common Errors:
- 400, "INVALID_PARAMETER"

<br>

Example of successful response:
```json
{
  "success": true,
  "lastUpdate": "2023-01-09T12:00:00Z",
  "data": {
    "count": 220,
    "list": [
      {
        "code": "USD",
        "rate": "1"
      },
      {
        "code": "EUR",
        "rate": "0.895772375876783"
      },
      ...
    ]
  }
}
```

{{< table "table-striped table-responsive" >}}
|      Field                        |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "success"                         | Boolean                | HTTP Request is successful, if it's false you have to [handle the error](/docs/quickstart/errors/) |
| "lastUpdate"                      | DateTime               | Latest data update time, depends on your [subscription plan](/docs/pricing/) |
| "data"                            | Object                 ||
| "data", "count"                   | Integer                | Length of the result list |
| "data", "list"                    | Array                  | Result list |
| "data", "list", \<element\>, "code" | String               | Listing code of the target asset |
| "data", "list", \<element\>, "rate" | Decimal string       | [Midmarket rate](/docs/quickstart/midmarket/) of the target date |
{{< /table >}}

<br>

> ⚠️ The decimal values are passed as strings to avoid loss of precision during the data transfer and JSON decode.
> You could parse them into a floating point value, but we advise you to use something like BigInteger.

<br><hr>

## Different Base Currency

Results can also be obtained in another base currency for conversion rates (other than the default USD).

In the following example, `1 EUR` = `1.11669349969065 USD`.

HTTP Request:
```
GET /history/base/{code}
```

<br>

HTTP Request Example:
```
GET /history/base/EUR?date=2023-01-10&type=currency&assets[]=USD&assets[]=EUR
```

<br>

{{< table "table-striped table-responsive" >}}
|      Parameter                    |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "date"                            | Date                   | Reference date of the daily conversion rate, using the `YYYY-MM-DD` format |
| "type"                            | String enum            | (Optional) Get only the specified type of assets, can be `currency`, `crypto`, `material` |
| "assets[]"                        | String array           | (Optional) Get only the specified assets listing codes |
{{< /table >}}

<br>

Common Errors:
- 400, "INVALID_PARAMETER"
- 404, "BASE_ASSET_NOT_FOUND"

<br>

Example of successful response:
```json
{
  "success": true,
  "lastUpdate": "2023-01-10T12:00:00Z",
  "data": {
    "count": 220,
    "list": [
      {
        "code": "USD",
        "rate": "1.11669349969065"
      },
      {
        "code": "EUR",
        "rate": "1"
      },
      ...
    ]
  }
}
```
