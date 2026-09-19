
# Error Reference

This page describes potential HTTP errors that may occur when working with the Reports API.

> **Documentation status:** The successful `200 OK` response has been verified through Postman. The error scenarios listed below are provided for documentation planning and require additional API testing for confirmation.

## HTTP Status Codes

| Status Code | Name | Description | Verification Status |
|---|---|---|---|
| `400` | Bad Request | The server cannot process the request because of invalid input. | Not verified |
| `401` | Unauthorized | The request requires valid authentication credentials. | Not verified |
| `403` | Forbidden | The server refuses to authorize the request. | Not verified |
| `404` | Not Found | The requested resource could not be found. | Not verified |
| `500` | Internal Server Error | The server encountered an unexpected condition. | Not verified |

## Error Testing Scenarios

The following scenarios can be used to plan additional API testing.

### 400 — Bad Request

**Scenario:** Send an invalid query parameter or unsupported parameter value.

**Expected outcome:** The API may return a `400 Bad Request` response if the request is invalid.

**Verification:** Not yet performed.

### 401 — Unauthorized

**Scenario:** Send the request without required authentication credentials, if authentication is supported.

**Expected outcome:** The API may return a `401 Unauthorized` response.

**Verification:** Not yet performed.

### 403 — Forbidden

**Scenario:** Send a request using credentials that do not have the required permissions, if authorization is supported.

**Expected outcome:** The API may return a `403 Forbidden` response.

**Verification:** Not yet performed.

### 404 — Not Found

**Scenario:** Request a resource or endpoint that does not exist.

**Expected outcome:** The API may return a `404 Not Found` response.

**Verification:** Not yet performed.

### 500 — Internal Server Error

**Scenario:** An unexpected server-side error occurs while processing the request.

**Expected outcome:** The API may return a `500 Internal Server Error` response.

**Verification:** Not yet performed.

## Error Handling Guidelines

When troubleshooting an API request:

1. Verify the request URL and HTTP method.
2. Check the query parameters and their values.
3. Confirm that the required headers are included.
4. Review the HTTP status code returned by the server.
5. Check the response body for additional error information.
6. Retry the request only after reviewing the cause of the error.

## Testing Notes

The following request was tested successfully using Postman:

```http
GET https://api.qaautomationlabs.com/v1/reports?page=1&limit=10
```

**Observed response:**

- HTTP status: `200 OK`
- Response format: JSON
- Header used: `Accept: application/json`

Error responses and authentication requirements should be added to this documentation after they are confirmed through API testing.
