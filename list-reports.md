Base URL
Request URL
Query Parameters
Parameter	Type	Description
page	integer	Specifies the page number to retrieve.
limit	integer	Specifies the maximum number of records to return.
Request Headers
Header	Value
Accept	application/json
cURL Example
Postman

Configure the request in Postman as follows.

Method
URL
Header

Click Send to execute the request.

Successful Response

The request returned 200 OK during testing.

Response Overview

The response contains a data array. Each item in the array represents a report.

For details about the response fields, see the
Response Reference.

HTTP Status Code
Status Code	Description
200 OK	The request was successfully processed and report data was returned.
Pagination

The endpoint accepts page and limit query parameters.

Example:

The page parameter identifies the requested page, while limit specifies the maximum number of records requested.

Pagination behavior beyond the parameters verified above is not documented until it has been tested against the API.
