
# Reports API Documentation

A practical REST API documentation project built with Markdown, Postman, MkDocs Material, and GitHub Pages.

This project demonstrates how technical writers can structure API documentation to help developers understand endpoints, configure requests, and interpret API responses.

[View API Reference](list-reports.md) · [About This Project](about.md)

---

## Project Overview

The Reports API provides access to generated reports through a RESTful API.

This documentation covers the request configuration, query parameters, response structure, and report object fields for the reports endpoint.

## API Information

| Item | Details |
|---|---|
| API Type | REST API |
| Base URL | `https://api.qaautomationlabs.com` |
| API Version | `v1` |
| Response Format | JSON |
| Documented Method | `GET` |

## Available Endpoint

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/v1/reports` | Retrieves a list of reports |

## Quick Start

### Request

```bash
curl -X GET "https://api.qaautomationlabs.com/v1/reports?page=1&limit=10" \
  -H "Accept: application/json"
```

### Request Parameters

| Parameter | Type | Description |
|---|---|---|
| `page` | integer | Specifies the page number to retrieve. |
| `limit` | integer | Specifies the maximum number of records requested. |

### Response

The endpoint returned a `200 OK` response during Postman testing.

The response contains a `data` array with report objects.

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

---

## Documentation Sections

| Section | Description |
|---|---|
| [List Reports](list-reports.md) | Request details, parameters, headers, and examples. |
| [Response Reference](response-reference.md) | Response structure and report object fields. |
| [Error Reference](errors.md) | Verified behavior and unverified error test scenarios. |
| [About This Project](about.md) | Project objectives, tools, and documentation approach. |

## Testing

The endpoint was tested using Postman to verify the request configuration, query parameters, response structure, and HTTP status code.

Only behavior verified during testing is documented as confirmed API behavior.

## Tools Used

- Markdown
- Postman
- GitHub
- MkDocs
- Material for MkDocs
- GitHub Pages
