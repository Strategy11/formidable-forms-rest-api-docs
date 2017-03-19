# Forms

## Get All forms

This endpoint retrieves an array of all forms.

### HTTP Request

`GET http://example.com/wp-json/frm/v2/forms`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 20 | Limit the number of forms returned
order | ASC | Use ASC or DESC
order_by | created_at | Order the entries by id, created_at, updated_at, form_id
page | 1 | The page number to retrieve.
page_size | 10 | Change the number of forms returned per page
return | array | Unknown
search | '' | Search all fields in the entries for a value.

### Pagination

Requests that return multiple items will be paginated to 10 items by default. The items per page can be specified with the `?page_size` parameter:

`GET /forms?page_size=15`

You can specify further pages with the `?page` parameter:

`GET /forms?page=2`

## Get a Single Form

This endpoint gets a single form.

`GET http://example.com/wp-json/frm/v2/forms/{formID}`

## Create a Form

This endpoint creates a single form.

`POST http://example.com/wp-json/frm/v2/forms/`

## Delete a Form

This endpoint deletes a single form.

`DELETE http://example.com/wp-json/frm/v2/forms/{formID}`
