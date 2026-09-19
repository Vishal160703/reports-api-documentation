
# Response Reference

This page describes the JSON response structure and fields returned by the Reports API.

## Response Structure

A successful request returns a JSON object containing a `data` array.

Each element in the `data` array represents a report object.

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

## Response Overview

| Property | Type | Description |
|---|---|---|
| `data` | array | Contains the report objects returned by the API. |

## Report Object

The report object contains information about an individual report.

| Field | Type | Description | Example |
|---|---|---|---|
| `id` | integer | Identifies the report. | `1` |
| `name` | string | Specifies the name of the report. | `"Sales Report 1"` |
| `type` | string | Specifies the report type. | `"sales"` |
| `format` | string | Specifies the report format. | `"pdf"` |
| `status` | string | Specifies the current report status. | `"ready"` |
| `rows` | integer | Specifies the number of rows associated with the report. | `20423` |
| `generatedAt` | string | Specifies the date and time associated with report generation. | `"2026-02-21T23:31:53+00:00"` |

## Field Details

### `id`

Identifies the report.

**Type:** `integer`

Example:

```json
{
  "id": 1
}
```

### `name`

Specifies the name of the report.

**Type:** `string`

Example:

```json
{
  "name": "Sales Report 1"
}
```

### `type`

Specifies the report type.

**Type:** `string`

Example:

```json
{
  "type": "sales"
}
```

### `format`

Specifies the report format.

**Type:** `string`

Example:

```json
{
  "format": "pdf"
}
```

### `status`

Specifies the current report status.

**Type:** `string`

Example:

```json
{
  "status": "ready"
}
```

### `rows`

Specifies the number of rows associated with the report.

**Type:** `integer`

Example:

```json
{
  "rows": 20423
}
```

### `generatedAt`

Specifies the date and time associated with report generation.

**Type:** `string`

Example:

```json
{
  "generatedAt": "2026-02-21T23:31:53+00:00"
}
```

> The date-time format and timezone behavior have not been independently verified beyond the returned example.

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

The following example is based on the response observed during Postman testing.

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

## Documentation Notes

- The `data` property was observed as an array in the tested response.
- The report fields are documented based on the returned JSON structure.
- Field validation rules and allowed values have not been independently verified.
- Additional response properties should be documented after they are confirmed through testing.
