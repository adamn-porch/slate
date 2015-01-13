# API

The API uses the standard technology of REST calls over HTTP.
  
Responses are returned in the JSON format.

## Changes

Our API is versioned off by version number in the URL (i.e. https://api.porch.com/v1, https://api.porch.com/v2). Advanced notification of breaking changes will be sent by email to our API users.

## Authentication

> To authorize, use this code:

```json
```

```java
```

```csharp
using System.Net.Http;

using (var client = new HttpClient())
{
    client.DefaultRequestHeaders.Add("api-key", "partnerApiKey");
    ...
}
```
```php
```

> Make sure to replace `partnerApiKey` with your API key.

This API is authenticated using an authorized API key in the headers of each request.

All requests are associated with a specific company’s API key and permissions are limited to that company’s capabilities.

Porch expects for the API key to be included in all API requests to the server in a header that looks like the following:

`api-key: partnerApiKey`

## Requests

The base URL of the API is https://api.porch.com/version where version should be replaced with the current version number (i.e. v1, v2).

JSON Bodies

All POST requests are JSON encoded and must have content type of application/json, or the API will return a 415 Unsupported Media Type status code.

HTTP Verbs

We use standard HTTP verbs to indicate intent of a request:

Method | Definition
---------- | -------
GET | To retrieve a resource or a collection of resources
POST | To create a resource

## Responses

All response bodies are JSON encoded.

A single resource is represented as a JSON object

`
{
  "field1": "value",
  "field2": true,
  "field3": []
}
`

A collection of resources is represented as a JSON array of objects

`
[
  {
    "field1": "value",
    "field2": true,
    "field3": []
  },
  {
    "field1": "another value",
    "field2": false,
    "field3": []
  }
]
`

Timestamps are formatted as Unix.

Unset fields will be represented as a null instead of not being present. If the field is an array, it will be represented as an empty array (i.e. []).

###HTTP Status Codes

We use HTTP status codes to indicate success or failure of a request.

Success Code | Meaning
---------- | -------
200 | OK -- Request succeeded. Response included
201 | Created -- Resource created. URL to new resource in Location header
204 | No Content -- Request succeeded, but no response body

Error Code | Meaning
---------- | -------
400 | Bad Request -- Could not parse request
401 | Unauthorized -- No authentication credentials provided or authentication failed
403 | Forbidden -- Authenticated user does not have access
404 | Not Found -- Resource not found
415 | Unsupported Media Type -- POST request occurred without an application/json content type
422 | Unprocessable Entry -- A request to modify or create a resource failed due to a validation error
500 | Not Found -- An internal server error occurred
501 | Not Found -- An internal server error occurred
502 | Not Found -- An internal server error occurred
503 | Not Found -- An internal server error occurred


###Client Errors
Some of the response errors will contain a message with the response code.

Response Code | Meaning
---------- | -------
401 | Unauthorized -- API Key required in headers
403 | Forbidden -- Invalid API Key
400 | Bad Request -- Listing property address required; Problem parsing listing property
