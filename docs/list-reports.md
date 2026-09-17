
# List Reports

Retrieves a list of generated reports.

## Endpoint

```http
GET /v1/reports
```

## Base URL

```text
https://api.qaautomationlabs.com
```

## Request URL

```text
https://api.qaautomationlabs.com/v1/reports?page=1&limit=10
```

## Query Parameters

| Parameter | Type | Description |
|---|---|---|
| `page` | integer | Specifies the page number to retrieve. |
| `limit` | integer | Specifies the maximum number of records to return. |

## Request Headers

| Header | Value |
|---|---|
| `Accept` | `application/json` |

## cURL Example

```bash
curl -X GET "https://api.qaautomationlabs.com/v1/reports?page=1&limit=10" \
  -H "Accept: application/json"
```

## Postman

Configure the request in Postman as follows.

### Method

```text
GET
```

### URL

```text
https://api.qaautomationlabs.com/v1/reports?page=1&limit=10
```

### Header

```text
Accept: application/json
```

Click **Send** to execute the request.

## Successful Response

The request returned `200 OK` during testing.

```json
{
  "data": [
    {
      "id": 1,
      "name": "Sales Report 1",
      "type": "sales",
      "format": "pdf",
      "status": "ready",
      "rows": 20423,
      "generatedAt": "2026-02-21T23:31:53+00:00"
    },
    {
      "id": 2,
      "name": "Sales Report 2",
      "type": "sales",
      "format": "pdf",
      "status": "ready",
      "rows": 18343,
      "generatedAt": "2026-02-12T21:16:45+00:00"
    }
  ]
}
```

## Response Overview

The response contains a `data` array. Each item in the array represents a report.

For details about the response fields, see the [Response Reference](response-reference.md).

## HTTP Status Code

| Status Code | Description |
|---|---|
| `200 OK` | The request was successfully processed and report data was returned. |

## Pagination

The endpoint accepts `page` and `limit` query parameters.

Example:

```text
/v1/reports?page=1&limit=10
```

The `page` parameter identifies the requested page, while `limit` specifies the maximum number of records requested.

> Pagination behavior beyond the parameters verified above is not documented until it has been tested against the API.
