
# Reports API Documentation

The Reports API provides access to generated reports through a RESTful API.

This documentation explains how to retrieve reports, configure request parameters, and interpret the API response.

## API Information

| Item | Details |
|---|---|
| API type | REST API |
| Base URL | `https://api.qaautomationlabs.com` |
| API version | `v1` |
| Response format | JSON |

## Authentication

Authentication requirements for this endpoint have not been documented because they were not verified during testing.

## Available Endpoint

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/v1/reports` | Retrieves a list of reports |

## Quick Example

```bash
curl -X GET "https://api.qaautomationlabs.com/v1/reports?page=1&limit=10" \
  -H "Accept: application/json"
```

The request returned a successful `200 OK` response during testing.

## Response

The API returns report records inside the `data` array.

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

## Documentation

- [List Reports](list-reports.md)
- [Response Reference](response-reference.md)
- [Error Reference](errors.md)

## Testing

The endpoint was tested using Postman to verify the request configuration, query parameters, response structure, and HTTP status code.
