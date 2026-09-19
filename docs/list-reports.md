
# List Reports

Retrieves a list of generated reports from the Reports API.

## Endpoint

| Item | Details |
|---|---|
| Method | `GET` |
| Endpoint | `/v1/reports` |
| Response format | JSON |

## Request URL

```text
https://api.qaautomationlabs.com/v1/reports?page=1&limit=10
```

## Query Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| `page` | integer | Not verified | Specifies the page number to retrieve. |
| `limit` | integer | Not verified | Specifies the maximum number of records requested. |

> **Note:** Whether these parameters are mandatory or optional has not been verified.

## Request Headers

| Header | Value | Description |
|---|---|---|
| `Accept` | `application/json` | Indicates that the client expects a JSON response. |

## cURL Example

```bash
curl -X GET "https://api.qaautomationlabs.com/v1/reports?page=1&limit=10" \
  -H "Accept: application/json"
```

## Postman Configuration

Use the following configuration to test the endpoint in Postman.

| Setting | Value |
|---|---|
| Method | `GET` |
| URL | `https://api.qaautomationlabs.com/v1/reports?page=1&limit=10` |
| Header | `Accept: application/json` |

### Steps

1. Open Postman.
2. Create a new HTTP request.
3. Select the `GET` method.
4. Enter the request URL.
5. Add the `Accept: application/json` header.
6. Click **Send**.
7. Review the HTTP status code and response body.

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

The response contains a `data` array. Each element represents a report object.

For information about the response fields, see the [Response Reference](response-reference.md).

## HTTP Status Code

| Status Code | Description |
|---|---|
| `200 OK` | The request was successfully processed, and report data was returned. |

## Pagination

The endpoint accepts `page` and `limit` query parameters.

Example:

```text
/v1/reports?page=1&limit=10
```

The meaning of the parameters is documented based on their use in the tested request. Additional pagination behavior has not been verified.

## Testing Notes

The endpoint was tested using Postman.

The verified test result was:

- HTTP status: `200 OK`
- Response format: JSON
- Response structure: Object containing a `data` array
