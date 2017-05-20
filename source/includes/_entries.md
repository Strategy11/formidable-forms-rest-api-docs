# Entries

## Get All Entries

This endpoint retrieves all entries.

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

### HTTP Request

`GET http://example.com/wp-json/frm/v2/entries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
form_id | 0 | Get all entries from a specific form
page | 1 | The page number to retrieve.
page_size | 25 | Change the number of entries returned
order | ASC | Use ASC or DESC
order_by | id | Order the entries by id, created_at, updated_at, form_id
search | | Search all fields in the entries for a value.

<aside class="notice">
Instead of using GET http://example.com/wp-json/frm/v2/entries?form_id=1 to get all entries from a specific form, you could also use the following HTTP Request.
</aside>

`GET http://example.com/wp-json/frm/v2/forms/1/entries`

### Pagination

Requests that return multiple items will be paginated to 25 items by default. The items per page can be specified with the `?page_size` parameter:

`GET /entries?page_size=15`

You can specify further pages with the `?page` parameter:

`GET /entries?page=2`

## Get a single entry by Entry ID

This endpoint retrieves a single entry using the Entry ID.

### HTTP Request

`GET http://example.com/wp-json/frm/v2/entries/{entry_id}`

## Create a single entry by Entry ID

This endpoint creates a single entry.

### HTTP Request

`POST http://example.com/wp-json/frm/v2/entries/{entry_id}`

## Update a single entry by Entry ID

These endpoints update a single entry.

### HTTP Request

`POST http://example.com/wp-json/frm/v2/entries/{entry_id}`

`PUT http://example.com/wp-json/frm/v2/entries/{entry_id}`

`PATCH http://example.com/wp-json/frm/v2/entries/{entry_id}`
