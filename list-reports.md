Request URL
Query Parameters
Parameter	Type	Required	Description
page	integer	No	Specifies the page number to retrieve.
limit	integer	No	Specifies the maximum number of reports to return.
Request Headers
Header	Value	Required	Description
Accept	application/json	No	Specifies that the client expects a JSON response.
Example Request
cURL
Postman

Configure the request in Postman as follows:

Method

URL

Header

Click Send to execute the request.

Successful Response

200 OK

Response

The response contains a data array. Each object in the array represents a report.

See Response Reference for details about the response fields.

HTTP Status Code
Status Code	Description
200 OK	The request was successfully processed and report data was returned.
Pagination

The endpoint accepts page and limit query parameters.

Example:

page=1 requests the first page.
limit=10 requests up to 10 records.
