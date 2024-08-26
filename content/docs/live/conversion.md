---
weight: 3
draft: false
toc: false
title: "Currency Conversion"
description: "API to convert a specific amount of an asset to another one"
---

> Available only in plans starting from [PRO](/docs/pricing/)

Convert a specified quantity of an asset to another one.

HTTP Request:
```
GET /live/conversion
```

<br>

{{< table "table-striped table-responsive" >}}
|      Parameter                    |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "quantity"                        | Number                 | Quantity of "from" asset to convert |
| "from"                            | String                 | Listing code of the asset to convert` |
| "to"                              | String                 | Listing code of the target asset of the conversion |
| "truncate"                        | Boolean                | (Optional, default: true) Specify if you want to truncate the converted result to the target asset significant decimal places |
{{< /table >}}

<br>

HTTP Request Example:
```
GET /live/conversion?quantity=10.5&from=USD&to=EUR
```

<br>

Common Errors:
- 400, "INVALID_PARAMETER"

<br>

Example of successful response:
```json
{
  "success": true,
  "lastUpdate": "2024-08-26T15:07:00.993Z",
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
