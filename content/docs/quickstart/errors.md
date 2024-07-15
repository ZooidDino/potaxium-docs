---
weight: 4
draft: false
toc: false
title: "Errors"
description: "Description of possible errors returned by the APIs"
---

Each success response returns the HTTP status code `200 OK` and contains the field
`"success": true` in the JSON body, along with the requested data.

For all the other cases, the response body will be like this:
```json
{
  "success": false,
  "error": "UNAUTHORIZED",
  "details": ""
}
```

- Details field is optional and may contain additional human-readable details about the error, in a string
- Error field is always a value present in the following table

{{< table "table-striped table-responsive" >}}
|      Response Code    |   Error                |  Description |
|:---------------------:|:----------------------:|:-------------|
| 400                   | "INVALID_PARAMETER"    | An invalid parameter was provided in the request, check the details field for more information |
| 401                   | "UNAUTHORIZED"         | The API key provided is invalid, or you don't have permissions to access the requested endpoint |
| 404                   | "ENDPOINT_NOT_FOUND"   | A non-existent endpoint was requested |
| 404                   | "ASSET_NOT_FOUND"      | The asset specified in the request doesn't exist |
| 404                   | "BASE_ASSET_NOT_FOUND" | The base asset specified in the request doesn't exist |
| 404                   | "HISTORY_NOT_FOUND"    | The value of the requested historical rate is not available |
| 405                   | "METHOD_NOT_ALLOWED"   | An existing endpoint was requested, but the wrong HTTP method was used in the request (e.g. `POST` instead of `GET`). |
| 500                   | "INTERNAL_SERVER_ERROR" | An unexpected error happened while processing the request, please [contact us](/docs/support) |
{{< /table >}}