# Introduction #

Welcome to the Formidable Forms API official documentation! The Formidable Forms API is fully integrated with the WordPress [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer) API. This allows Formidable data to be created, read, updated, and deleted using requests in JSON format and using WordPress REST API Authentication methods and standard HTTP verbs which are understood by most HTTP clients.

The following table shows API versions present in each major version of WooCommerce:

| API Version |   FF Version   |  WP Version  |       Documentation       |
|-------------|----------------|--------------|---------------------------|
| `v2`        |        -       | 4.4 or later | -                         |
| `v1`        |        -       | 4.4 or later | [v1 docs](v1.html) |

## Requirements ##
To use the latest version of the REST API you must be using:

* Formidable 2.0+
* Formidable API 1.0+
* WordPress 4.4+
* Pretty permalinks in Settings > Permalinks so that the custom endpoints are supported. Default permalinks will not work.
* You may access the API over either HTTP or HTTPS, but HTTPS is recommended where possible.

## Download and install ##
1. Download the latest version of the [Formidable API add-on](https://formidableforms.com/downloads/formidable-api/).
2. In your WordPress admin, go to 'Plugins' → 'Add New' and click the 'Upload Plugin' button at the top of the page.
3. Upload the zip file you just downloaded in step two. Once the plugin is installed, click 'Activate Plugin' or go to the 'Plugins' page, find 'Formidable API' and click 'Activate'.

## HTTP Methods ##

### GET ###
Make a GET request to retrieve data. GET requests will never cause an update or change to your data because they’re safe and [idempotent](https://developer.mozilla.org/en-US/docs/Glossary/idempotent).

### POST ###
Use a POST request to create new entries, forms, Views, or fields. POST can also be used to update an entry, form, View, or field.

### PATCH ###
Make a PATCH request to update an entry, form, View, or field. With PATCH requests, you only need to provide the data you want to change.

### PUT ###
Use a PUT request to create or update an entry, form, View, or field.

### DELETE ###
Make a DELETE request to delete an entry, form, View, or field.

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

## Tools ##

Some useful tools you can use to access the API include:

- [Postman](https://www.getpostman.com/) - A multi platform REST API GUI client (using Google Chrome or installing the app on Mac OS X or Windows).
- [CocoaRestClient](http://mmattozzi.github.io/cocoa-rest-client/) - A Mac OS X GUI client for interacting with the API.
- [Paw HTTP Client](https://itunes.apple.com/us/app/paw-http-client/id584653203?mt=12) - Another HTTP client for Mac OS X.
- [RESTClient, a debugger for RESTful web services](https://addons.mozilla.org/en-US/firefox/addon/restclient/) - Free Firefox add-on.
- [Advanced REST client](https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo) - Free Google Chrome extension.
