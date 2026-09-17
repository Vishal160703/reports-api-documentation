
# Response Reference

This page describes the response structure and fields returned by the Reports API.

## Response Structure

A successful request returns a JSON object containing a `data` array.

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

## Top-Level Fields

| Field | Type | Description |
|---|---|---|
| `data` | array | Contains the report objects returned by the API. |

## Report Object

Each item in the `data` array represents a report.

| Field | Type | Description |
|---|---|---|
| `id` | integer | Identifies the report. |
| `name` | string | Specifies the name of the report. |
| `type` | string | Specifies the type of the report. |
| `format` | string | Specifies the format of the report. |
| `status` | string | Specifies the current status of the report. |
| `rows` | integer | Specifies the number of rows associated with the report. |
| `generatedAt` | string | Specifies the date and time associated with report generation. |

## Field Details

### `id`

Identifies the report.

Example:

```json
"id": 1
```

### `name`

Specifies the name of the report.

Example:

```json
"name": "Sales Report 1"
```

### `type`

Specifies the type of the report.

Example:

```json
"type": "sales"
```

### `format`

Specifies the format of the report.

Example:

```json
"format": "pdf"
```

### `status`

Specifies the current status of the report.

Example:

```json
"status": "ready"
```

### `rows`

Specifies the number of rows associated with the report.

Example:

```json
"rows": 20423
```

### `generatedAt`

Specifies the date and time associated with report generation.

Example:

```json
"generatedAt": "2026-02-21T23:31:53+00:00"
```

## Complete Report Object

```json
{
  "id": 1,
  "name": "Sales Report 1",
  "type": "sales",
  "format": "pdf",
  "status": "ready",
  "rows": 20423,
  "generatedAt": "2026-02-21T23:31:53+00:00"
}
```

## Example Response

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
