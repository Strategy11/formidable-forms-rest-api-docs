# Introduction

Welcome to the Formidable Forms API official documentation! The Formidable Forms API is fully integrated with the WordPress [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer) API. This allows Formidable data to be created, read, updated, and deleted using requests in JSON format and using WordPress REST API Authentication methods and standard HTTP verbs which are understood by most HTTP clients.

## Requirements
To use the latest version of the REST API you must be using:

* Formidable 2.0+
* Formidable API 1.0+
* WordPress 4.4+
* Pretty permalinks in Settings > Permalinks so that the custom endpoints are supported. Default permalinks will not work.
* You may access the API over either HTTP or HTTPS, but HTTPS is recommended where possible.

## Request/Response Format ##

The default response format is JSON. Requests with a message-body use plain JSON to set or update resource attributes. Successful requests will return a `200 OK` HTTP status.

## Errors ##

Occasionally you might encounter errors when accessing the REST API. There are four possible types:

| Error Code | Error Type |
|------------|------------|
| `400 Bad Request` | Invalid request, e.g. using an unsupported HTTP method | 
| `401 Unauthorized` | Authentication or permission error, e.g. incorrect API keys |
| `403 Forbidden` | Your API key didn't log you in. If you are using Basic Authentication, your server may not be recognizing your authorization headers. |
| `404 Not Found` | Requests to resources that don't exist or are missing |
| `500 Internal Server Error` | Server error |

> WP REST API error example:

```json
{
  "code": "rest_no_route",
  "message": "No route was found matching the URL and request method",
  "data": {
    "status": 404
  }
}
```

Errors return both an appropriate HTTP status code and response object which contains a `code`, `message` and `data` attribute.

## Parameters ##

Almost all endpoints accept optional parameters which can be passed as a HTTP query string parameter, e.g. `GET /entries?search=Test`. All parameters are documented along each endpoint.
