# Entries

## Get All Entries

This endpoint retrieves all entries.

### HTTP Request

`GET http://example.com/wp-json/frm/v2/entries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
order_by | id | Order the entries by id, created_at, updated_at, form_id
order | ASC | Use ASC or DESC
page | 1 | The page number to retrieve.
page_size | 25 | Change the number of entries returned
search | | Search all fields in the entries for a value.

