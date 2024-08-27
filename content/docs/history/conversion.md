---
weight: 3
draft: false
toc: false
title: "Currency Conversion"
description: "API to convert a specific amount of an asset to another one using the fx rates of a specified date"
---

> Available only in plans starting from [PRO](/docs/pricing/)

Convert a specified quantity of an asset to another one using the conversion rate of a specified date, when available.
Availability of conversion rates depends upon the date and it doesn't correspondent to all the assets with live conversion.
The availability of conversion rates depends on the date and doesn't correspond to all currently available live assets.

HTTP Request:
```
GET /history/conversion
```

<br>

{{< table "table-striped table-responsive" >}}
|      Parameter                    |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "date"                            | Date                   | Reference date of the daily conversion rate, using the `YYYY-MM-DD` format |
| "quantity"                        | Number                 | Quantity of "from" asset to convert |
| "from"                            | String                 | Listing code of the asset to convert` |
| "to"                              | String                 | Listing code of the target asset of the conversion |
| "truncate"                        | Boolean                | (Optional, default: true) Specify if you want to truncate the converted result to the target asset significant decimal places |
{{< /table >}}

> ⚠️ Minimum supported date is 2000-01-01

<br>

HTTP Request Example:
```
GET /history/conversion?date=2023-01-30&quantity=10.5&from=USD&to=EUR
```

<br>

Common Errors:
- 400, "INVALID_PARAMETER"
- 404, "HISTORY_NOT_FOUND"

<br>

Example of successful response:
```json
{
  "success": true,
  "lastUpdate": "2023-01-30T12:00:00Z",
  "data": "9.39"
}
```

{{< table "table-striped table-responsive" >}}
|      Field                        |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "success"                         | Boolean                | HTTP Request is successful, if it's false you have to [handle the error](/docs/quickstart/errors/) |
| "lastUpdate"                      | DateTime               | Latest data update time, depends on your [subscription plan](/docs/pricing/) |
| "data"                            | Decimal string         | Result of requested asset conversion |
{{< /table >}}

<br>

> ⚠️ The decimal values are passed as strings to avoid loss of precision during the data transfer and JSON decode.
> You could parse them into a floating point value, but we advise you to use something like BigInteger.
