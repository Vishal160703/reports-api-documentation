Use this endpoint to retrieve a list of reports.

Quick Example
Example Response
Documentation
List Reports
Response Reference
Testing

The API was tested using Postman to verify the request, query parameters, response, and HTTP status code.

Related Tools
Postman
cURL
Markdown
MkDocs Material
Step 2 — Create the actual endpoint page

After committing, go back to the repository home.

Again:

Add file → Create new file

File name:

Paste:

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

HTTP 200 OK

The API returns a JSON response containing the reports in the data array.

Response

The response contains a data array. Each object in the array represents a report.

For information about the individual response fields, see Response Reference.

HTTP Status Code
Status Code	Description
200 OK	The request was successfully processed and report data was returned.
Pagination

The endpoint accepts page and limit query parameters.

Example:

page=1 requests the first page.
limit=10 requests up to 10 records.

The behavior of additional pagination parameters should be verified against the API before documenting them.

Step 3 — Create the response reference

Create:

Paste:

Response Fields
data
Property	Type	Description
data	array	Contains the report objects returned by the API.
Report Object
Property	Type	Description
id	integer	Unique identifier of the report.
name	string	Name of the report.
type	string	Type of report.
format	string	Format of the report.
status	string	Current status of the report.
rows	integer	Number of rows contained in the report.
generatedAt	string	Date and time associated with report generation.
