
# API Testing with Postman

This page documents the API testing process used to validate the Reports API request and response.

Postman was used to send the API request, inspect the HTTP response, and review the returned JSON data.

## Testing Tool

| Item | Details |
|---|---|
| Tool | Postman |
| API Type | REST API |
| HTTP Method | GET |
| Response Format | JSON |
| Test Objective | Validate the API request and response structure |

## API Request

The following endpoint was tested using Postman:

```http
GET https://api.qaautomationlabs.com/v1/reports?page=1&limit=10
```

### Request Components

| Component | Value |
|---|---|
| Method | `GET` |
| Endpoint | `https://api.qaautomationlabs.com/v1/reports` |
| Query Parameter | `page=1` |
| Query Parameter | `limit=10` |

## Request Headers

The following header was included in the request:

| Header | Value | Purpose |
|---|---|---|
| `Accept` | `application/json` | Indicates that the client expects a JSON response. |

### Example Request

```http
GET /v1/reports?page=1&limit=10
Accept: application/json
```

## Test Execution

The request was sent using Postman.

The response was reviewed to check:

1. HTTP status code.
2. Response format.
3. JSON response structure.
4. Report object fields.
5. Returned report data.

## Observed Response

The request returned the following result during testing:

| Item | Observed Value |
|---|---|
| HTTP Status | `200 OK` |
| Response Format | JSON |
| Response Body | Contains a `data` array |
| Report Fields | ID, name, type, format, status, rows, and generated date |

### Sample Response

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
    }
  ]
}
```

## Test Observations

The following observations were recorded during the test:

- The API returned an HTTP `200 OK` status.
- The response was returned in JSON format.
- The response contained a `data` array.
- Each report object contained report-related fields.
- The response structure was used to prepare the API response reference documentation.

## Documentation Workflow

The API testing results supported the following documentation activities:

1. Identifying the API endpoint and HTTP method.
2. Documenting the request header.
3. Reviewing the JSON response structure.
4. Identifying response fields and their data types.
5. Creating request and response examples.
6. Documenting potential error-testing scenarios.

## Testing Limitations

The following items require additional testing before they can be documented as verified behavior:

- Authentication requirements.
- Invalid query parameter handling.
- Authentication and authorization errors.
- Resource-not-found behavior.
- Server-side error responses.
- Pagination behavior beyond the tested request.

## Summary

Postman testing helped validate the successful API response and provided the information required to create the API reference and response documentation.

Additional test cases should be performed before documenting unverified API behavior as confirmed functionality.
