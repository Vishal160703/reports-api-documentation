
# Error Reference

This page describes error handling considerations for the Reports API.

## Verified Response

The Reports API endpoint was successfully tested using Postman.

| Item | Verified Value |
|---|---|
| HTTP Method | `GET` |
| Endpoint | `/v1/reports` |
| Response Status | `200 OK` |
| Response Format | JSON |

## Error Testing

Only the successful `200 OK` response has been verified so far.

Specific error status codes and response bodies should be documented only after they are tested against the API.

## Error Scenarios to Test

The following scenarios can be tested to identify how the API handles invalid or incomplete query parameters.

| Scenario | Example Request |
|---|---|
| Invalid page value | `/v1/reports?page=abc&limit=10` |
| Invalid limit value | `/v1/reports?page=1&limit=abc` |
| Missing page parameter | `/v1/reports?limit=10` |
| Missing limit parameter | `/v1/reports?page=1` |
| Very large page value | `/v1/reports?page=999999&limit=10` |

## Error Response Documentation

When an error response is verified, document the following information:

| Information | Description |
|---|---|
| HTTP status code | Status code returned by the API. |
| Error message | Message returned by the API. |
| Response body | JSON structure returned for the error. |
| Resolution | Recommended action to resolve the error. |

> **Note:** The error responses and scenarios listed above have not been verified against the API. They are test scenarios only and should not be treated as confirmed API behavior.
