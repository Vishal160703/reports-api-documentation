The request returned a successful 200 OK response during testing.

Response

The API returns report records inside the data array.

Documentation
List Reports
Response Reference
Error Reference
Testing

The endpoint was tested using Postman to verify the request configuration, query parameters, response structure, and HTTP status code.

Base URL
Request URL
Query Parameters
Parameter	Type	Required	Description
page	integer	No	Specifies the page number to retrieve.
limit	integer	No	Specifies the maximum number of records to return.
Example

In this example:

page=1 requests the first page.
limit=10 requests up to 10 records.
Request Headers
Header	Value	Required	Description
Accept	application/json	No	Indicates that the client expects a JSON response.
cURL Example
Postman

Configure the request in Postman as follows.

Method
URL
Header

Click Send to execute the request.

Successful Response

HTTP 200 OK

Response Overview

The response contains a data array. Each item in the array represents a report.

For information about the fields returned for each report, see Response Reference.

HTTP Status Code
Status Code	Description
200 OK	The request was successfully processed and report data was returned.
Pagination

The endpoint accepts page and limit query parameters.

For example:

The page parameter identifies the requested page, while limit specifies the maximum number of records requested.

Pagination behavior beyond the parameters verified above is not documented until it has been tested against the API.

Top-Level Fields
Field	Type	Description
data	array	Contains the report objects returned by the API.
Report Object

Each item in the data array represents a report.

Field	Type	Description
id	integer	Unique identifier of the report.
name	string	Name of the report.
type	string	Type of the report.
format	string	Format of the report.
status	string	Current status of the report.
rows	integer	Number of rows associated with the report.
generatedAt	string	Date and time associated with report generation.
Field Details
id

Identifies the report.

Example:

name

Specifies the name of the report.

Example:

type

Specifies the report type.

Example:

format

Specifies the report format.

Example:

status

Specifies the current report status.

Example:

rows

Specifies the number of rows associated with the report.

Example:

generatedAt

Specifies the date and time associated with report generation.

Example:

Complete Report Object
