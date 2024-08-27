---
weight: 2
draft: false
toc: false
title: "Historical Range Data"
description: "API to retrieve the forex conversion rates of a single pair in a specified date range"
---

> Available only in plans starting from [MINIMAL](/docs/pricing/)

Obtain a list of all the daily conversion rates of a specified asset pairs using a custom time range.

The maximum time range specified in a single request is 100 days.

HTTP Request:
```
GET /history/range/daily
```

<br>

{{< table "table-striped table-responsive" >}}
|      Parameter                    |   Type                 |  Description |
|:---------------------------------:|:----------------------:|:-------------|
| "from"                            | String                 | Listing code of the first asset (e.g. `EUR`) |
| "to"                              | String                 | Listing code of the second asset (e.g. `USD`) |
| "start"                           | Date                   | Start date of the daily rate range, using the `YYYY-MM-DD` format |
| "end"                             | Date                   | End date of the daily rate range, using the `YYYY-MM-DD` format |
{{< /table >}}

> ⚠️ Minimum supported date is 2000-01-01

<br>

HTTP Request Example (`EUR-USD` pair):
```
GET /history/range/daily?from=EUR&to=USD?start=2023-01-09&end=2023-01-12
```

<br>

Common Errors:
- 400, "INVALID_PARAMETER"

<br>

Example of successful response:
```json
{
  "success": true,
  "lastUpdate": "2024-08-27T00:00:00Z",
  "data": {
    "count": 4,
    "list": [
      {
        "date": "2023-01-09",
        "rate": "1.075709892180262"
      },
      {
        "date": "2023-01-10",
        "rate": null
      },
      {
        "date": "2023-01-11",
        "rate": "1.074434285403087"
      },
      {
        "date": "2023-01-12",
        "rate": "1.0823576976472"
      }
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
| "data", "list", \<element\>, "date" | Date                 | Reference date of the specified rate, using the `YYYY-MM-DD` format |
| "data", "list", \<element\>, "rate" | Decimal string       | [Midmarket rate](/docs/quickstart/midmarket/) of the target date, if it's null the value is missing for the request date |
{{< /table >}}

<br>

> ⚠️ The decimal values are passed as strings to avoid loss of precision during the data transfer and JSON decode.
> You could parse them into a floating point value, but we advise you to use something like BigInteger.
